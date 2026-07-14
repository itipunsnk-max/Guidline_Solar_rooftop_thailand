# รายงาน Preliminary Assessment — Solar Rooftop ประเทศไทย

**สถานะ:** Need More Data (ไม่ใช่แบบก่อสร้างหรือคำขออนุญาต)  
**วันที่ตรวจข้อมูล/เข้าถึงแหล่งอ้างอิง:** 15 กรกฎาคม 2569 (2026)  
**ฐานข้อมูลโครงการ:** ไฟล์ `pasted-text.txt` ที่ผู้ใช้ให้มา

## 1. ข้อสรุปสำหรับผู้บริหาร

ไฟล์ต้นทางกำหนดขอบเขตงานครบถ้วนสำหรับโครงการ Solar Rooftop ตั้งแต่สำรวจ ออกแบบ การเงิน ใบอนุญาต ก่อสร้าง O&M และการขออนุมัติงบประมาณ แต่ **ยังไม่มีข้อมูลโครงการจริง**: ชื่อ/ตำแหน่งไซต์, ผู้ให้บริการไฟฟ้า, รูปแบบลงทุน, ขนาดหม้อแปลง, โหลด, พื้นที่หลังคา, แบบโครงสร้าง, SLD, งบประมาณ และความต้องการ BESS เป็นช่อง `[ระบุ]` ทั้งหมด

จึงยังไม่สามารถระบุอย่างน่าเชื่อถือได้ว่า

- ขนาด PV ที่ควรติดตั้ง, จำนวนแผง/อินเวอร์เตอร์ หรือพื้นที่ใช้จริง
- ผลิตไฟฟ้า, self-consumption, export, PR, P50/P90 หรือค่า CO2 ที่ลดได้
- CAPEX/OPEX, Payback, NPV, IRR, LCOE และทางเลือกที่คุ้มค่าที่สุด
- ความสามารถของหลังคา จุดเชื่อมต่อ และเงื่อนไข MEA/PEA ที่ใช้บังคับ
- ใบอนุญาตที่ต้องยื่นจริง

**ข้อเสนอเพื่ออนุมัติในขั้นนี้:** อนุมัติเฉพาะ “การเก็บข้อมูลและสำรวจความเป็นไปได้” ไม่อนุมัติการลงทุน EPC จนกว่าจะผ่านเงื่อนไขในส่วน 17 การติดตั้งเพื่อใช้เองบนหลังคาอาจใช้ช่องทางแจ้งการประกอบกิจการที่ได้รับยกเว้นตาม กกพ. ได้ในกรณีที่เข้าเกณฑ์ แต่ต้องตรวจเงื่อนไขไซต์และการไฟฟ้าเป็นรายกรณี; กรณีระบบ inverter รวมตั้งแต่ 200 kVA หรือ 200 kW ขึ้นไป กกพ. ระบุว่าต้องพิจารณาใบอนุญาตผลิตพลังงานควบคุม (พค.2) ด้วย [กกพ.](https://www.erc.or.th/th/installed-on-the-roof)

## 2. คำจำกัดความและขอบเขต

| รายการ | Preliminary scope | นอกขอบเขตจนกว่าจะมีข้อมูล |
|---|---|---|
| เทคนิค | checklist, design basis, จุดตัดสินใจ และรายการคำนวณที่ต้องทำ | แบบ IFC, string plan, protection setting, structural calculation |
| ไฟฟ้า | ตรวจรายการข้อมูล MDB/transformer/SLD และแนวทาง interconnection | short-circuit, load flow, harmonic, coordination study |
| โครงสร้าง | กำหนดหลักฐานที่ต้องใช้และเกณฑ์ส่งต่อวิศวกร | รับรองความมั่นคงแข็งแรง/ออกแบบเสริมกำลัง |
| การเงิน | โมเดลและตัวแปรที่ต้องใช้ | ตัวเลขเงินลงทุน/ผลตอบแทนจริง |
| อนุญาต | permit matrix แบบมีเงื่อนไข | ยืนยันว่าข้อยกเว้นหรือใบอนุญาตใดใช้จริง |

**เกณฑ์การตัดสินใจที่เสนอ:** (1) หลังคาได้รับการรับรอง, (2) ระบบไฟฟ้าและจุดเชื่อมต่อผ่านการศึกษา, (3) self-consumption และความเสี่ยง export ผ่านเกณฑ์องค์กร, (4) ผลตอบแทนผ่าน hurdle rate, (5) ใบอนุญาต/เงื่อนไขการไฟฟ้าไม่มีข้อห้าม, (6) แผนความปลอดภัยและช่วง shutdown ได้รับอนุมัติ

## 3. Checklist เตรียมข้อมูลก่อนสำรวจ

| ลำดับ | รายการ/รายละเอียดที่ต้องตรวจ | หลักฐาน | ผู้รับผิดชอบ | สถานะ |
|---:|---|---|---|---|
| 1 | ค่าใช้ไฟ 12–24 เดือน: kWh, kW, demand, tariff/TOU | บิลและไฟล์ meter | เจ้าของไซต์/การเงิน | ขาด |
| 2 | โหลดราย 15 นาทีหรือรายชั่วโมง และแผนขยายโหลด | CSV/EMS/BMS | วิศวกรรมโรงงาน | ขาด |
| 3 | ขนาด/อายุ/พิกัดหม้อแปลง, MDB, breaker, busbar | nameplate, SLD, maintenance record | Electrical | ขาด |
| 4 | ตำแหน่งจุดเชื่อมต่อ, CT/มิเตอร์, generator/ATS | SLD/รูปถ่าย | Electrical | ขาด |
| 5 | แบบหลังคา/โครงสร้าง, อายุ, ประวัติรั่วซึม | structural/as-built drawing | Civil/เจ้าของอาคาร | ขาด |
| 6 | พื้นที่หลังคา, ทางเดิน, skylight, ช่องเปิด และเงา | roof plan/ภาพโดรน | Site/EPC | ขาด |
| 7 | จังหวัด/พิกัด, MEA หรือ PEA และสภาพแวดล้อม | ที่อยู่/GPS | เจ้าของไซต์ | ขาด |
| 8 | ข้อจำกัด HSE, hazardous area, งานบนที่สูง/เวลาหยุดงาน | HSE plan, area classification | HSE | ขาด |
| 9 | เป้าหมายธุรกิจ, CAPEX/PPA/ESCO, hurdle rate และ COD | business brief | ผู้บริหาร/การเงิน | ขาด |
| 10 | BESS: วัตถุประสงค์, กำลัง/เวลา backup, fire strategy | load criticality study | Owner/HSE/Electrical | ขาด |

## 4. แบบสำรวจหน้างานที่ต้องปิดก่อนออกแบบ

### 4.1 สถานที่และหลังคา

- บันทึก GPS, ทิศ/มุมหลังคา, elevation, ภาพ 360°, สิ่งปลูกสร้างและเงาบังตามเวลา
- ตรวจชนิดหลังคา, ความลาดเอียง, การกัดกร่อน, จุดรั่ว, อายุคงเหลือ, ขอบหลังคา, skylight/vent และทางหนีไฟ
- วัดพื้นที่สุทธิหลังหัก setback, ทางเดิน, fire access และพื้นที่ห้ามติดตั้ง
- จัดทำ shading scene และ horizon profile สำหรับ PVsyst; ห้ามใช้ค่าผลผลิตจากค่าเฉลี่ยทั่วไปแทนการจำลองตามพิกัด

### 4.2 โครงสร้าง

- รวบรวมแบบ/สำรวจแป จันทัน คาน เสา รอยต่อ และสภาพ corrosion
- วิศวกรโครงสร้างต้องตรวจน้ำหนักคงที่ของแผง/ราง/สาย, น้ำหนักจรสำหรับบำรุงรักษา, แรงลมยก และการถ่ายแรงเข้าสู่โครงสร้างเดิม
- ยืนยันรายละเอียดการยึดและ waterproofing ตามชนิดหลังคา ก่อนสั่งซื้อวัสดุ; หากไม่มีแบบเดิมหรือมีความเสียหาย ให้ทำ survey/calculation หรือเสริมกำลังก่อนตัดสินใจ

### 4.3 ระบบไฟฟ้าและความปลอดภัย

- ตรวจแรงดัน/เฟส/ความถี่, short-circuit rating, protection coordination, CT/VT/meter, quality ของกำลังไฟ, earthing, lightning protection และ SPD
- ตรวจระยะ/route สาย DC-AC, จุดตัดแยก, inverter location, ventilation, ingress protection และพื้นที่ BESS (ถ้ามี)
- ระบุ anti-islanding, export-control/zero-export, generator/ATS interaction และ commissioning tests
- จัดทำ work-at-height, rescue, lockout/tagout, lifting, emergency shutdown และ fire plan; หากเป็นสถานีบริการน้ำมัน/พื้นที่อันตราย ให้ยืนยัน area classification และวิศวกรผู้มีใบอนุญาตก่อนออกแบบ

## 5. Standards Register (Preliminary)

**ชั้นการใช้:** “กฎหมาย/ใบอนุญาต” ต้องปฏิบัติตามเมื่อเข้าเกณฑ์, “ข้อกำหนดการไฟฟ้า” เป็นเงื่อนไขเชื่อมต่อ, “IEC/มาตรฐานอ้างอิง” ใช้กำหนดสเปกเมื่อสัญญาหรือหน่วยงานอ้างถึง ไม่ใช่สิ่งทดแทนกฎหมายไทย

| มาตรฐาน/ข้อกำหนด | เจ้าของ/สถานะวันที่ 15 ก.ค. 2026 | ประเด็นใช้ | ระดับ | สถานะ |
|---|---|---|---|---|
| กฎ/คู่มือใบอนุญาตกิจการไฟฟ้า | กกพ. | exemption, licence, เอกสาร SLD/วิศวกร | กฎหมาย/กำกับ | ตรวจใน permit matrix |
| พค.2 และขั้นตอน | พพ. | ระบบ rooftop ที่เข้าเกณฑ์ controlled energy | กฎหมาย | ตรวจขนาด inverter รวม |
| ข้อกำหนด interconnection/inverter ของ MEA หรือ PEA | การไฟฟ้าพื้นที่ | capacity, approved equipment, test ก่อน parallel | เงื่อนไขบังคับ | ต้องเลือกการไฟฟ้าก่อน |
| IEC 60364-7-712:2025 | IEC/TC 64 | การติดตั้ง PV supply system | อ้างอิงออกแบบ | ยืนยันฉบับที่สัญญา/ไทยรับรอง |
| IEC 62548-1:2023 + AMD1:2025 | IEC/TC 82 | array, DC wiring, protection, switching, earthing, mounting | อ้างอิงออกแบบ | ตรวจแล้วจาก IEC |
| IEC 62446-1:2016 + AMD1:2018 | IEC/TC 82 | documentation, inspection, commissioning | อ้างอิงทดสอบ | ตรวจแล้วจาก IEC |
| IEC 61215-1:2021 | IEC/TC 82 | design qualification PV module | สเปกผลิตภัณฑ์ | ตรวจแล้วจาก IEC |
| IEC 61730-1:2023 (และ Part 2 ที่เกี่ยวข้อง) | IEC/TC 82 | safety qualification module | สเปกผลิตภัณฑ์ | ตรวจแล้วจาก IEC |
| IEC 62109 series | IEC/TC 82 | safety of PV power converters | สเปกผลิตภัณฑ์ | ตรวจ edition/Part 2 ก่อนสเปก |
| มาตรฐาน วสท., มอก., มาตรฐานอาคาร/แรงลม และมาตรฐานพื้นที่อันตราย | หน่วยงานเจ้าของ | installation/earth/lightning/structure/fire | ตามกฎหมายหรือสัญญา | **ต้องยืนยันเลข/edition จากต้นฉบับก่อนออกแบบ** |

ไม่ระบุเลข edition ของ วสท., มอก., มาตรฐานแรงลม หรือเอกสาร MEA/PEA ในรายงานนี้ เพราะไฟล์ต้นทางไม่มีเอกสารอ้างอิงเฉพาะและยังไม่ได้ยืนยันฉบับล่าสุดจากเจ้าของมาตรฐานโดยตรง

## 6. Design Basis และทางเลือกออกแบบ

### Design basis ที่ต้องอนุมัติก่อน Preliminary Design

| หัวข้อ | ค่าในรายงานนี้ | ต้องยืนยันจาก |
|---|---|---|
| พิกัด, meteo, GHI/temperature | ยังไม่มี | ที่อยู่/GPS และฐานข้อมูล meteo ที่เลือก |
| DC/AC capacity, DC/AC ratio, module/inverter | ยังไม่กำหนด | load profile, roof layout, utility requirement |
| orientation/tilt | ยังไม่กำหนด | survey/structural/wind/shading analysis |
| export | ยังไม่กำหนด | MEA/PEA และรูปแบบธุรกิจ |
| cable/protection/earthing/SPD | ยังไม่กำหนด | SLD, fault level, study และมาตรฐานที่ใช้ |
| degradation, availability, O&M | **สมมติฐานไม่ได้รับอนุมัติ** | warranty, O&M scope, model assumptions |

**ทางเลือกที่ต้องประเมินหลังได้ข้อมูล**

| ทางเลือก | หลักตัดสิน | ผลลัพธ์ที่ต้องแสดง | ความเสี่ยงหลัก |
|---|---|---|---|
| A Maximum self-consumption | จับคู่ generation กับโหลดรายช่วงเวลา | kWp/kWac, 12 เดือน generation/offset/export, economics | โหลดกลางวันต่ำ/curtailment |
| B Maximum available roof area | จำกัดด้วยโครงสร้าง, rooftop usable area, interconnection | layout, structural impact, export-control, economics | export/transformer/หลังคา |
| C Economic optimum | NPV/IRR ภายใต้เงื่อนไของค์กร | sensitivity, capex/opex, payback, risk | tariff และสมมติฐานผลผลิต |

สำหรับทุกทางเลือก ต้องยืนยัน module Voc ที่อุณหภูมิต่ำสุด, Isc, MPPT range, maximum system voltage, string count, cable voltage drop, protection selectivity และ export setting จาก datasheet/การศึกษา ไม่คำนวณจากค่าเฉลี่ยหรือจากชื่อรุ่นอุปกรณ์

## 7. PVsyst Input/Output Checklist

**Input บังคับ:** พิกัด, meteo database/version, horizon, 3D shading scene, module/inverter datasheet, tilt/azimuth, strings/MPPT, cable losses, soiling, availability, grid limitation, load profile, tariff และ degradation

**Output ที่ต้องตรวจทาน:** GHI/POA/effective irradiation, specific yield, PR, loss diagram, monthly generation, clipping/shading/temperature/mismatch losses, self-consumed/exported/curtailed energy, energy injected และ P50/P90 เมื่อมีฐานข้อมูลและวัตถุประสงค์รองรับ

**เกณฑ์ QA:** บันทึก version ของ PVsyst และ meteo, peer-review shading และ string configuration, reconcile generation กับ load profile, และอธิบายทุก loss. ผลจำลองก่อนข้อมูลครบเป็น “scenario” เท่านั้น ไม่ใช่ guarantee

## 8. แบบจำลองไฟฟ้าและการเงิน

### 8.1 สูตร/ข้อมูลที่ต้องใช้

| ตัวแปร | สถานะ | แหล่งที่ยอมรับ |
|---|---|---|
| Annual/monthly PV generation | ขาด | PVsyst จาก design ที่ตรวจแล้ว |
| self-consumption/export/curtailment | ขาด | load interval + generation interval |
| tariff และ demand saving | ขาด | บิล/อัตราค่าไฟของลูกค้า |
| CAPEX, contingency, VAT | ขาด | ใบเสนอราคา EPC เทียบเคียงอย่างน้อยตาม procurement policy |
| O&M, insurance, cleaning, inverter replacement | ขาด | scope, warranty, tender quote |
| discount rate, tax, escalation, salvage | ขาด | นโยบายการเงินองค์กร |

โมเดล 25 ปีต้องแสดง cash flow รายปี, CAPEX, OPEX, replacement, degradation, tax (หากใช้), payback/discounted payback, NPV, IRR, ROI, LCOE และ B/C ratio พร้อมหน่วย/วันที่ฐานราคา ทุกตัวเลขที่ยังไม่ได้รับเอกสารต้นทางต้องติดป้าย **สมมติฐาน**

### 8.2 BOQ โครงสร้าง (ไม่มีราคา)

PV module; inverter; mounting; DC/AC cable และ tray; combiner/isolator/fuse/SPD; ACDB/MDB modification; metering/protection/SCADA; earthing/lightning; roof waterproofing/structural reinforcement; installation/lifting/temporary works; design/T&C/utility application; HSE; O&M; contingency; insurance/warranty reserve; VAT. ราคาต่อ Wp หรือ budgetary cost **ไม่เสนอ** เพราะไม่มีขนาด ระบบ สเปก สถานที่ หรือราคาอ้างอิงวันที่เดียวกัน

### 8.3 Sensitivity ที่ต้องทำ

CAPEX +10/+20%; ค่าไฟ -10/-20%; yield -5/-10%; escalation; degradation สูงขึ้น; inverter replacement เร็ว; curtailment/zero export; outage; roof reinforcement; และ BESS. ต้องแสดงผลต่อ NPV/IRR/payback ไม่ใช้เพียงความเห็นเชิงคุณภาพ

## 9. Permit Matrix และ workflow

| หน่วยงาน | เรื่องที่ต้องตรวจ | Trigger/หลักฐาน | สถานะ |
|---|---|---|---|
| MEA หรือ PEA | ขอเชื่อมต่อ, ความจุ, inverter ที่ยอมรับ, test/parallel | พื้นที่บริการ, application, SLD/datasheet/แบบวิศวกร | ขาดพื้นที่และ SLD |
| กกพ. | exemption notification หรือใบอนุญาตประกอบกิจการ | รูปแบบใช้เอง/ขายไฟ, ขนาด, สัญญา, เอกสารเทคนิค | ต้องคัดกรองเป็นรายโครงการ |
| พพ. | พค.2 | inverter grid-connected รวมตั้งแต่ 200 kVA หรือ 200 kW ตามหน้ากกพ. | ต้องทราบ kW/kVA inverter |
| เจ้าพนักงานท้องถิ่น | ดัดแปลงอาคาร/เอกสารโครงสร้าง | วิธีติดตั้ง/น้ำหนัก/ลักษณะอาคาร/กฎหมายท้องถิ่น | ต้องตรวจพื้นที่จริง |
| กรมโรงงานฯ/หน่วยงานโรงงาน | ใบอนุญาตหรือการแจ้งที่เกี่ยวข้อง | ประเภทโรงงานและการเปลี่ยนแปลง | ต้องตรวจใบ รง.4/เงื่อนไขไซต์ |
| หน่วยงานสิ่งแวดล้อม/ท้องถิ่น | EIA/ข้อยกเว้น, fire/environment | ประเภท/ขนาด/พื้นที่โครงการ | ต้องคัดกรอง |
| HSE/อัคคีภัย | WAH, electrical safety, fire plan, hazardous area | งาน/พื้นที่/ผู้รับเหมา | ต้องจัดทำก่อนเริ่มงาน |

**Workflow:** เก็บข้อมูล → สำรวจ/structural & electrical assessment → preliminary design/PVsyst → pre-check interconnection → decision gate งบประมาณ → detailed design/permit submission → procurement → construction ตาม HSE/ITP → test/commission → utility parallel/COD → handover/O&M. ระบบตรวจสอบขนาดของ MEA เป็นเพียง pre-check; ผลที่ยืนยันต้องมาจากการยื่นขอเชื่อมต่อ [MEA](https://spv.mea.or.th/check-capacity)

## 10. Construction, QA/QC และ O&M

ก่อนก่อสร้างต้องออก Method Statement, ITP, QC Plan, HSE/WAH/Lifting/Electrical Safety/Fire Emergency/Shutdown Plan, T&C Plan และ as-built plan. Hold/Witness points ขั้นต่ำ: รับวัสดุและใบรับรอง; structural fixing/waterproofing; DC routing/polarity/insulation; earthing/SPD/termination; protection setting; Voc/Isc/IV curve (ถ้ากำหนด); anti-islanding; power quality; synchronization; monitoring; PR baseline.

ส่งมอบอย่างน้อย: as-built drawings/SLD, datasheets/certificates, commissioning records, warranty matrix, spare list, O&M manual, preventive/corrective schedule, cleaning/thermography/IR/earthing/inverter/SPD/roof inspection, alarm/escalation process, response time และ performance/availability method ที่ตกลงในสัญญา

## 11. Risk Register

| ความเสี่ยง | ผลกระทบ | ระดับก่อนควบคุม | มาตรการ/เงื่อนไขปิดความเสี่ยง | Owner |
|---|---|---|---|---|
| หลังคา/แรงลมรับไม่พอ | รุนแรงมาก | สูง | signed structural assessment และ fixing/waterproofing detail | Structural engineer |
| น้ำรั่ว/กัดกร่อน | สูง | สูง | roof condition survey, approved detail, warranty | Civil/EPC |
| เงาบัง/ผลผลิตต่ำ | กลาง–สูง | สูง | survey + PVsyst 3D scene + uncertainty review | PV engineer |
| transformer/MDB/protection ไม่รองรับ | รุนแรงมาก | สูง | SLD, load/fault/coordination/interconnection study | Electrical engineer |
| reverse power/export/harmonic | สูง | สูง | utility decision, meter/export-control/settings test | Electrical/EPC |
| ฟ้าผ่า/DC arc/ไฟไหม้ | รุนแรงมาก | สูง | design to approved standards, SPD/earthing, fire plan, emergency isolation | Electrical/HSE |
| ใบอนุญาตล่าช้า | กลาง–สูง | สูง | permit owner, matrix, pre-consultation, critical-path tracking | PM |
| ราคา/lead time | กลาง | กลาง | dated quotations, contingency, approved alternates | Procurement |
| ธุรกิจหยุดไม่ได้/งานบนที่สูง | รุนแรงมาก | สูง | outage plan, phased work, WAH/rescue plan | PM/HSE |
| monitoring cyber risk | กลาง | กลาง | access control, network segregation, patching/ownership | IT/O&M |
| BESS (ถ้ามี) | รุนแรงมาก | สูง | separate battery/fire/electrical study; do not add by default | Owner/HSE/Electrical |

## 12. Proposal และ Approval Memo (ร่างพร้อมกรอก)

**หัวเรื่อง:** ขออนุมัติการศึกษาความเป็นไปได้และออกแบบเบื้องต้นโครงการ Solar Rooftop ณ [ชื่อไซต์]

**คำขออนุมัติ:** อนุมัติงบสำหรับ site survey, structural/electrical studies, PVsyst, utility pre-check และการจัดทำแบบ/ใบอนุญาตเบื้องต้น โดยยังไม่ผูกพันการจัดซื้อ EPC

**เหตุผล:** เพื่อยืนยันขนาดระบบที่สอดคล้องกับโหลดและหลังคา ลดความเสี่ยงด้านโครงสร้าง/ไฟฟ้า/ใบอนุญาต และทำให้ผลตอบแทนได้รับการตรวจสอบก่อนอนุมัติลงทุน

**สิ่งที่จะส่งกลับเพื่อขออนุมัติลงทุน:** ทางเลือก A/B/C พร้อม energy yield, self-consumption/export, CAPEX/BOQ และข้อเสนอราคา, 25-year financial model/sensitivity, structural/electrical studies, permit status, HSE/risk plan และ implementation schedule

**ไม่ควรกล่าวอ้างใน Proposal ปัจจุบัน:** ขนาดติดตั้ง, เงินประหยัด, payback, NPV/IRR, CO2 reduction หรือกำหนด COD ที่แน่นอน เนื่องจากไม่มีข้อมูลรองรับ

## 13. แผนงานระดับ Preliminary

| Stage | ผลส่งมอบ | เงื่อนไขเริ่ม/จบ |
|---|---|---|
| 0 Data room | รายการข้อมูลครบ | ได้บิล/โหลด/SLD/แบบ/พิกัด |
| 1 Site survey | survey + roof/electrical gap list | เข้าไซต์ได้และมีผู้ประสานงาน |
| 2 Studies | structural/electrical/PVsyst preliminary | ข้อมูลสำคัญผ่าน QA |
| 3 Options | A/B/C + financial model | tariff/quotes/utility basis ยืนยัน |
| 4 Permits/approval | permit matrix และ CAPEX request | เลือกแนวทางลงทุน |
| 5 EPC/COD | detailed design → construction → test | อนุมัติลงทุนและใบอนุญาตพร้อม |

ไม่กำหนดจำนวนวันหรือ COD เพราะเวลาขึ้นกับข้อมูล, การสำรวจ, การอนุมัติ MEA/PEA/หน่วยงาน, procurement และข้อจำกัดการหยุดระบบ

## 14. ข้อมูลขาด และคำถามถึงเจ้าของพื้นที่ (15 ข้อ)

1. ชื่อโครงการ, ที่อยู่, จังหวัด และพิกัด GPS คืออะไร?  
2. อาคารและกิจการเป็นประเภทใด; มีพื้นที่อันตราย/สถานีบริการน้ำมันหรือไม่?  
3. พื้นที่อยู่ใน MEA หรือ PEA และเลขผู้ใช้ไฟ/สัญญาใด?  
4. รูปแบบธุรกิจที่ต้องการคือ self-consumption, export sale, CAPEX, PPA หรือ ESCO?  
5. ส่งบิลไฟ 12–24 เดือนและ tariff/demand/TOU ได้หรือไม่?  
6. มีไฟล์ load profile 15 นาที/ชั่วโมง และแผนขยายโหลดหรือไม่?  
7. หม้อแปลง, MDB, breaker, short-circuit rating และ SLD เดิมเป็นเท่าใด?  
8. มี generator/ATS, existing PV หรือ BESS หรือไม่?  
9. พื้นที่หลังคาที่ใช้ได้ ชนิดหลังคา อายุ และประวัติรั่วซึมเป็นอย่างไร?  
10. มีแบบสถาปัตย์/โครงสร้าง/as-built และรายงานวิศวกรหรือไม่?  
11. มีเงาบัง, ข้อจำกัด fire access, skylight, ปล่อง หรืออุปกรณ์บนหลังคาใดบ้าง?  
12. ต้องเดินระบบโดยไม่หยุดผลิตหรือมี shutdown window ใด?  
13. BESS มีวัตถุประสงค์อะไรและต้องการ backup กี่ kW/kWh/ชั่วโมง?  
14. เกณฑ์ลงทุน (งบ, payback, IRR/NPV, อายุโครงการ, COD) คืออะไร?  
15. มีข้อกำหนด procurement, warranty, brand, cyber/IT และผู้มีอำนาจอนุมัติใดบ้าง?  

## 15. Final Decision Gate

**ผลการตัดสินใจปัจจุบัน: Need More Data**

จะเปลี่ยนเป็น “Proceed with Conditions” ได้เมื่อ: (1) ได้คำตอบ 15 ข้อและเอกสารหลักฐาน, (2) หลังคาผ่านการรับรองวิศวกร, (3) electrical/interconnection study ผ่าน, (4) ได้ฐาน tariff และ quotation เพื่อ financial model, (5) ระบุเส้นทางอนุญาตและผู้รับผิดชอบ, (6) HSE/ไฟไหม้/งานบนที่สูงผ่านการทบทวน. “Proceed” ต้องมีเอกสารปิดเงื่อนไขทั้งหมดและอำนาจอนุมัติลงทุนขององค์กร

## 16. แหล่งอ้างอิงหลัก

เข้าถึง 15 กรกฎาคม 2026; ระดับความน่าเชื่อถือ: **สูง** สำหรับหน่วยงานกำกับ/เจ้าของมาตรฐาน, **ต้องยืนยันเฉพาะโครงการ** สำหรับการใช้จริง

1. [กกพ. — Solar Rooftop และการแจ้ง/ยกเว้น](https://www.erc.or.th/th/installed-on-the-roof) — ข้อมูลเส้นทาง exemption, SLD/วิศวกร และเงื่อนไข พค.2
2. [กกพ. — แบบคำขอ/คู่มือใบอนุญาตประกอบกิจการไฟฟ้า](https://www.erc.or.th/th/application-forms/)
3. [กกพ. — การแจ้งเริ่มประกอบกิจการไฟฟ้า](https://www.erc.or.th/th/electrical-operations-notice)
4. [พพ. — การขออนุญาตผลิตพลังงานควบคุม](https://www.dede.go.th/articles?id=676) — หน้าข้อมูลปรับปรุง 16 กรกฎาคม 2025
5. [MEA — ระบบตรวจสอบขนาดกำลังผลิตเพื่อขอเชื่อมต่อ](https://spv.mea.or.th/check-capacity) — เป็นการตรวจสอบเบื้องต้นเท่านั้น
6. [IEC 62548-1:2023](https://webstore.iec.ch/en/publication/64171) และ [AMD1:2025](https://webstore.iec.ch/en/publication/98955)
7. [IEC 62446-1:2016/AMD1:2018](https://webstore.iec.ch/en/publication/61011)
8. [IEC 61215-1:2021](https://webstore.iec.ch/en/publication/61345)
9. [IEC 61730-1:2023](https://webstore.iec.ch/en/publication/59803)
10. [IEC 60364-7-712:2017 catalogue record](https://webstore.iec.ch/en/publication/28213) — หน้า IEC ระบุว่ามีฉบับ 2025; ต้องตรวจซื้อ/อ้างอิงฉบับ 2025 จาก catalogue ก่อนออกแบบ

> หมายเหตุ: กฎหมาย/ข้อกำหนดท้องถิ่น, เอกสาร MEA/PEA เฉพาะรุ่นอุปกรณ์ และมาตรฐาน วสท./มอก. ต้องตรวจฉบับล่าสุดจากเจ้าของเอกสารและยืนยันการใช้บังคับกับไซต์ก่อนยื่นแบบหรือจัดซื้อ
