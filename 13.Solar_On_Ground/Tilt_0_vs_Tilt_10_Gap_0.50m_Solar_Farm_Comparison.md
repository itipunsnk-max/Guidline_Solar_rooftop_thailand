# เปรียบเทียบ Solar Farm: Tilt 0° vs Tilt 10° ที่ Gap 0.50 m

> **กรณีศึกษา:** แผงวางแบบ Solar Farm / Slab-on-ground, ความยาวโต๊ะตามแนวลาดประมาณ **2.626 m**, เปรียบเทียบ `Tilt 0°` กับ `Tilt 10°` โดยคง **Gap = 0.50 m**  
> **วัตถุประสงค์:** เปรียบเทียบผลด้าน Pitch, GCR, Row-to-row shading, Energy Yield และการใช้พื้นที่

---

## 1. Executive Summary

จากการเปรียบเทียบเบื้องต้น:

- `Tilt 0°` ไม่มี row-to-row shading จากความสูงต่างระดับของแถว
- `Tilt 10° / Gap 0.50 m` มีโอกาสเกิด mutual shading โดยเฉพาะช่วงดวงอาทิตย์ต่ำ
- อย่างไรก็ตาม `Tilt 10°` ได้ประโยชน์จากการรับรังสีบนระนาบเอียง และสามารถวางแถวได้ถี่ขึ้นเล็กน้อย
- จาก screening estimate ปัจจุบัน:
  - Near-shading irradiance loss ของ Tilt 10° ประมาณ **1.5–2.1%**
  - หากรวม electrical mismatch แบบ conservative อาจอยู่ประมาณ **2.5–3.0%**
  - Tilt gain จาก 0° → 10° ประเมินเบื้องต้นประมาณ **+2–3%**
- ดังนั้นในแง่ `kWh/kWp` ทั้งสองกรณีอาจ **ใกล้เคียงกัน**
- แต่ในแง่ `kWh/m²` และการใช้งานจริง `Tilt 10°` มีแนวโน้ม **คุ้มค่ากว่า** เพราะใช้พื้นที่ได้หนาแน่นกว่าเล็กน้อย และระบายน้ำ/ทำความสะอาดได้ดีกว่า

> **ข้อสรุปเบื้องต้น:**  
> สำหรับงาน Solar Farm ที่ต้องการ maximize พลังงานต่อพื้นที่ แนะนำให้ใช้ **Tilt 10° / Gap 0.50 m** เป็น economic case แล้วตรวจสอบซ้ำด้วย **PVsyst Near Shading + Module Layout** ก่อนสรุป Final Design

---

## 2. Input Geometry

กำหนด:

| Parameter | Symbol | Value |
|---|---:|---:|
| ความยาวแผง/โต๊ะตามแนวลาด | $L$ | 2.626 m |
| Gap ระหว่างแถว | $G$ | 0.50 m |
| Tilt Case 1 | $\beta_0$ | 0° |
| Tilt Case 2 | $\beta_{10}$ | 10° |

---

## 3. สูตรที่ใช้

### 3.1 Horizontal Projected Width

ความกว้างของโต๊ะเมื่อฉายลงบนแนวราบ:

```math
W_h = L\cos(\beta)
```

---

### 3.2 Row Pitch

Pitch วัดจากตำแหน่งอ้างอิงของแถวหนึ่งไปยังแถวถัดไป:

```math
P = L\cos(\beta) + G
```

---

### 3.3 Ground Coverage Ratio (GCR)

สำหรับตารางนี้ใช้:

```math
GCR = \frac{L}{P}
```

โดย:

- $L$ = ความยาว collector ตามแนวลาด
- $P$ = Row Pitch

> หมายเหตุ: นิยาม GCR ในซอฟต์แวร์หรือเอกสารบางแห่งอาจระบุรูปแบบต่างกัน จึงควรใช้ definition เดียวกันตลอดทั้งโครงการ

---

## 4. คำนวณ Tilt 0°

### 4.1 Horizontal Width

เมื่อ:

```math
\beta = 0^\circ
```

จะได้:

```math
W_{h,0}
=
2.626\cos(0^\circ)
=
2.626\,\mathrm{m}
```

### 4.2 Pitch

```math
P_0
=
2.626 + 0.50
=
3.126\,\mathrm{m}
```

### 4.3 GCR

```math
GCR_0
=
\frac{2.626}{3.126}
=
0.840
```

ดังนั้น:

```math
\boxed{GCR_0 \approx 0.84}
```

---

## 5. คำนวณ Tilt 10°

### 5.1 Horizontal Width

```math
W_{h,10}
=
2.626\cos(10^\circ)
```

```math
W_{h,10}
\approx
2.586\,\mathrm{m}
```

### 5.2 Pitch

```math
P_{10}
=
2.586 + 0.50
=
3.086\,\mathrm{m}
```

### 5.3 GCR

```math
GCR_{10}
=
\frac{2.626}{3.086}
=
0.851
```

ดังนั้น:

```math
\boxed{GCR_{10} \approx 0.85}
```

---

## 6. เปรียบเทียบ Geometry

| Parameter | Tilt 0° | Tilt 10° / Gap 0.50 m |
|---|---:|---:|
| Collector length | 2.626 m | 2.626 m |
| Horizontal projected width | 2.626 m | 2.586 m |
| Gap | 0.50 m | 0.50 m |
| Pitch | **3.126 m** | **3.086 m** |
| GCR | **0.84** | **0.85** |
| Row-to-row beam shading | ต่ำมาก/ไม่มีจาก Tilt | มี |
| Drainage | ไม่ดี | **ดีกว่า** |
| Natural rain cleaning | ไม่ดี | **ดีกว่า** |
| Land-use density | Base | **สูงกว่าเล็กน้อย** |

---

## 7. ความได้เปรียบด้านจำนวนแถวต่อพื้นที่

เมื่อใช้พื้นที่แนว North–South เท่ากัน จำนวนแถวโดยประมาณจะแปรผกผันกับ Pitch

ดังนั้นอัตราการเพิ่มความหนาแน่นของแถวของ Tilt 10° เทียบกับ Tilt 0° กำหนดให้ `R_density` = Row Density Gain:

```math
R_{\mathrm{density}}
=
\frac{P_0}{P_{10}}-1
```

แทนค่า:

```math
R_{\mathrm{density}}
=
\frac{3.126}{3.086}-1
```

```math
R_{\mathrm{density}} \approx 0.0129
```

หรือ:

```math
\boxed{R_{\mathrm{density}} \approx 1.3\%}
```

กล่าวคือ ในพื้นที่แนว North–South เท่ากัน `Tilt 10°` สามารถติดตั้ง collector ได้มากขึ้นประมาณ **1.3%** เมื่อเทียบกับ `Tilt 0°` ภายใต้ geometry นี้

---

## 8. เปรียบเทียบ Energy Loss / Gain

### 8.1 Tilt 0°

ข้อดี:

- ไม่มี mutual shading ที่เกิดจากความสูงของแผงแต่ละแถว
- Geometry เรียบง่าย

ข้อเสีย:

- รับ irradiation บนระนาบแผงต่ำกว่าการเอียงเล็กน้อยในหลายช่วงของปี
- น้ำระบายออกจากผิวแผงได้ไม่ดี
- มีความเสี่ยงด้าน soiling / น้ำขัง / คราบบริเวณกรอบแผงมากกว่า

---

### 8.2 Tilt 10° / Gap 0.50 m

Screening estimate จาก sensitivity case ปัจจุบัน:

```math
L_{\mathrm{shade,irr}}
\approx
1.5\%-2.1\%
```

หากเผื่อ electrical mismatch จาก partial shading แบบ conservative:

```math
L_{\mathrm{shade,total}}
\approx
2.5\%-3.0\%
```

ขณะเดียวกัน การเปลี่ยนจาก 0° → 10° อาจได้ irradiation/transposition gain โดยประมาณ:

```math
G_{\mathrm{tilt}}
\approx
2\%-3\%
```

ดังนั้นผลสุทธิแบบ simplified screening สามารถเขียนได้เป็น:

```math
\Delta Y
\approx
G_{\mathrm{tilt}}
-
L_{\mathrm{shade}}
```

หากพิจารณาเฉพาะ irradiance shading:

```math
\Delta Y
\approx
(2\%-3\%)
-
(1.5\%-2.1\%)
```

จึงได้ช่วงประมาณ:

```math
\boxed{0\% \lesssim \Delta Y \lesssim +1.5\%}
```

> ค่านี้เป็น **screening estimate** ไม่ใช่ผล PVsyst final simulation

หากใช้ conservative electrical shading loss ประมาณ 2.5–3.0%:

```math
\Delta Y_{\mathrm{cons}}
\approx
(2\%-3\%)
-
(2.5\%-3.0\%)
```

ดังนั้น `kWh/kWp` ของ Tilt 0° และ Tilt 10° อาจออกมา **ใกล้เคียงกันมาก**

---

## 9. ผลต่อ Energy per Land Area

Energy ต่อพื้นที่สามารถมองอย่างง่ายได้จาก:

```math
E_{\text{land}}
\propto
\mathrm{PowerDensity}
\times
\mathrm{SpecificYield}
```

โดย Tilt 10° มี Row Density Gain ประมาณ:

```math
+1.3\%
```

ดังนั้น แม้ Specific Yield (`kWh/kWp`) จะใกล้เคียงกับ Tilt 0° แต่เมื่อคิด Installed MWp บนพื้นที่เดียวกัน Tilt 10° อาจให้พลังงานต่อพื้นที่สูงกว่าโดยประมาณ **1–2%**:

```math
\boxed{
1.01 \lesssim
\frac{E_{\mathrm{land},10}}{E_{\mathrm{land},0}}
\lesssim 1.02
}
```

**ทั้งนี้ต้องตรวจสอบด้วย Site-specific PVsyst simulation**

---

## 10. ตารางสรุปเชิงวิศวกรรม

| หัวข้อ | Tilt 0° | Tilt 10° / Gap 0.50 m | ผู้ได้เปรียบ |
|---|---:|---:|---|
| Pitch | 3.126 m | **3.086 m** | Tilt 10° |
| GCR | 0.84 | **0.85** | Tilt 10° |
| จำนวนแถวต่อพื้นที่ | Base | **+1.3%** | Tilt 10° |
| Row shading | **ต่ำกว่า** | สูงกว่า | Tilt 0° |
| Irradiance on plane | ต่ำกว่า | **สูงกว่า** | Tilt 10° |
| Drainage | แย่ | **ดี** | Tilt 10° |
| Natural cleaning | แย่ | **ดีกว่า** | Tilt 10° |
| Risk of standing water | สูงกว่า | **ต่ำกว่า** | Tilt 10° |
| kWh/kWp | ใกล้เคียง | ใกล้เคียง | ~Tie |
| kWh/m² land | Base | **มีแนวโน้มสูงกว่า** | Tilt 10° |
| Recommended for farm | ไม่แนะนำเป็นหลัก | **Recommended economic case** | Tilt 10° |

---

## 11. Recommendation

สำหรับ preliminary design แนะนำ **Tilt 10° / Gap 0.50 m**:

```math
\boxed{
\beta = 10^\circ,\qquad G = 0.50\,\mathrm{m}
}
```

ค่าหลัก:

```math
\boxed{
P \approx 3.086\,\mathrm{m}
}
```

```math
\boxed{
GCR \approx 0.85
}
```

และควรเผื่อ shading loss สำหรับ initial feasibility:

```math
\boxed{
L_{\mathrm{shade,total}}
\approx
2.5\%-3.0\%
}
```

ก่อนทำ Final Design ควรรัน PVsyst อย่างน้อย 2 Variant:

1. `Tilt = 0° / Gap = 0.50 m`
2. `Tilt = 10° / Gap = 0.50 m`

แล้วเปรียบเทียบค่า:

- `GlobInc`
- `GlobShd`
- `Near Shadings: Irradiance Loss`
- `Electrical Shading Loss`
- `EArray`
- `E_Grid`
- `Specific Production (kWh/kWp/year)`
- `Performance Ratio`
- `Installed MWp`
- `MWh/year per rai`
- `LCOE`

> จุดตัดสินที่ถูกต้องไม่ควรดูเพียง `% shading loss` แต่ควรดู **Annual Energy per Land Area และ LCOE** ของทั้งโครงการ

---

## 12. ข้อควรระวัง

ค่าประมาณในเอกสารนี้ยังไม่ได้รวมรายละเอียด site-specific เช่น:

- พิกัด Latitude / Longitude
- Meteo file
- Azimuth จริง
- Terrain slope
- Horizon profile
- Module electrical layout
- String orientation
- Bypass diode arrangement
- Diffuse shading
- Albedo
- Bifacial gain
- Soiling
- First-row / edge effects

ดังนั้นค่า shading loss `1.5–2.1%` และ conservative electrical shading `2.5–3.0%` ควรใช้เป็น **Design Screening Allowance** เท่านั้น

---

## 13. Reference

### PVsyst Documentation

PVsyst อธิบายว่าในการจัดแผงแบบ sheds การเพิ่ม Tilt จะเพิ่ม transposition gain แต่ในขณะเดียวกัน mutual shading ก็เพิ่มขึ้น และการหา optimum เป็นปัญหาแบบหลายตัวแปรที่ต้องพิจารณาทั้ง Yield, GCR, Installed Power และต้นทุน

- PVsyst — Sheds tilt optimization tool  
  https://www.pvsyst.com/help/project-design/orientations-in-v8/shed-optimization.html

- PVsyst — Sheds optimization tool  
  https://www.pvsyst.com/help/project-design/simulation/optimization-tool/index.html

- PVsyst — Transposition factor optimizing tool  
  https://www.pvsyst.com/help/project-design/orientations-in-v8/orientation-optimization.html

PVsyst ยังระบุแนวคิดสำคัญว่า low tilt มักเหมาะกับ shed systems เมื่อเป้าหมายคือเพิ่ม installed PV power ต่อพื้นที่ แต่ Tilt ที่ต่ำมากต้องพิจารณาผลต่อการระบายน้ำและการทำความสะอาดด้วย

---

## 14. Final Conclusion

> **Tilt 0°** ชนะด้านไม่มี row-to-row shading แต่เสียเปรียบด้าน drainage, soiling และการรับ irradiation บนระนาบแผง

> **Tilt 10° / Gap 0.50 m** แม้มี shading loss แต่ได้ Tilt gain กลับมา และมี Pitch สั้นลง ทำให้ติดตั้งแผงต่อพื้นที่ได้มากขึ้นประมาณ **1.3%**

ดังนั้นสำหรับ Solar Farm ที่ต้องการความคุ้มค่าด้านพื้นที่ **Tilt 10° / Gap 0.50 m มีแนวโน้มคุ้มค่ากว่า Tilt 0°**:

```math
\boxed{
\beta = 10^\circ,\qquad G = 0.50\,\mathrm{m}
}
```

โดย Final Decision ควรยืนยันจาก **PVsyst hourly simulation + Near Shading + Electrical Effect + LCOE comparison**.
