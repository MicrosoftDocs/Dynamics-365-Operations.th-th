---
# required metadata
title: เริ่มต้นใช้งานการจัดการบริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: หัวข้อนี้จะอธิบายวิธีการเริ่มต้นใช้งานการออกใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: null
ms.technology: null
ms.search.form: null
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: null
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: '2020-07-08'
ms.dyn365.ops.version: AX 10.0.12
---

# <a name="get-started-with-electronic-invoicing-service-administration"></a>เริ่มต้นใช้งานการจัดการบริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะดำเนินการกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์ ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้:

- คุณต้องมีสิทธิ์เข้าถึงบัญชี Microsoft Dynamics Lifecycle Services (LCS) ของคุณ
- คุณต้องมีโครงการ LCS ที่มีรุ่น 10.0.17 หรือใหม่กว่าของ Microsoft Dynamics 365 Finance หรือ Dynamics 365 Supply Chain Management นอกจากนี้ แอปเหล่านี้ต้องถูกปรับใช้ในหนึ่งในภูมิศาสตร์ Azure ต่อไปนี้:

    - สหรัฐ
    - ยุโรป
    - สหราชอาณาจักร
    - เอเชีย

- คุณต้องมีสิทธิ์เข้าถึงบัญชี Dynamics 365 Regulatory Configuration Services (RCS) ของคุณ
- คุณต้องเปิดใช้งานคุณลักษณะที่ใช้ทั่วโลกสำหรับบัญชี RCS ของคุณในการจัดการคุณลักษณะ สำหรับข้อมูลเพิ่มเติม ดู [Regulatory Configuration Services (RCS) - คุณลักษณะที่ใช้ทั่วโลก](rcs-globalization-feature.md)
- คุณต้องสร้าง Key Vault และบัญชีการจัดเก็บใน Azure สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>ติดตั้ง add-in สำหรับไมโครเซอร์วิสใน Lifecycle Services

1. ลงชื่อเข้าใช้บัญชี LCS และแดชบอร์ดโครงการ LCS ให้เลือกโครงการ LCS ของคุณ
2. ในโครงการ บนแดชบอร์ด **สภาพแวดล้อม** ให้เลือกโครงการที่ปรับใช้ของคุณ สภาพแวดล้อมที่คุณเลือกต้องทำงานอยู่
3. บนแท็บ **การรวม Power Platform** ในฟิลด์ **Add-in ของสภาพแวดล้อม** ให้เลือก **ติดตั้ง Add-in ใหม่**
4. เลือก **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
5. ในฟิลด์ **รหัสแอปพลิเคชัน AAD** ให้ป้อน **091c98b0-a1c9-4b02-b62c-7753395ccabe** ค่านี้เป็นค่าคงที่
6. ในฟิลด์ **รหัสผู้เช่า AAD** ป้อนรหัสผู้เช่าของบัญชีสมัครสมาชิก Azure ของคุณ ผู้เช่า Azure Active Directory (Azure AD) ที่คุณระบุควรเป็นผู้เช่าเดียวกันกับที่ใช้กับ RCS
7. ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือกกล่องกาเครื่องหมาย
8. เลือก **ติดตั้ง** การติดตั้งอาจใช้เวลาหลายนาที


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>ตั้งค่าพารามิเตอร์สำหรับการรวม RCS กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **การตั้งค่าที่เกี่ยวข้อง** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**
3. บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URI ปลายทางของบริการ** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้

    | ภูมิศาสตร์ของ Datacenter Azure | URI ปลายทางของบริการ                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | สหรัฐ              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ยุโรป                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | สหราชอาณาจักร             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | เอเชีย                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสแอปพลิเคชัน** เป็น **0cdb527f-a8d1-4bf8-9436-b352c68682b2** ค่านี้เป็นค่าคงที่
5. ในฟิลด์ **รหัสสภาพแวดล้อม LCS** ป้อนรหัสของสภาพแวดล้อม LCS ของคุณ
6. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="create-key-vault-references"></a>สร้างการอ้างอิง Key Vault

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
3. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**
4. เลือก **สร้าง** เพื่อสร้างการอ้างอิง Key Vault
5. ในฟิลด์ **ชื่อ** ป้อนชื่อสำหรับการอ้างอิง Key Vault ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
6. ในฟิลด์ **URI ของ Key URI** ให้วางข้อมูลลับของ Key Vault จาก Azure Key Vault สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)
7. เลือก **บันทึก**

## <a name="create-storage-account-secret"></a>สร้างข้อมูลลับของบัญชีที่จัดเก็บ

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** > **พารามิเตอร์ Key Vault**
2. เลือก **การอ้างอิง Key Vault** และในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**
3. ในฟิลด์ **ชื่อ** ป้อนชื่อข้อมูลลับของบัญชีที่จัดเก็บ สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)
4. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
5. ในฟิลด์ **ชนิด** เลือก **ข้อมูลลับ**
6. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="create-a-digital-certificate-secret"></a>สร้างความลับของใบรับรองดิจิทัล

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ** และจากนั้น เลือก **พารามิเตอร์ Key Vault**
2. เลือก **การอ้างอิง Key Vault** และจากนั้น ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**
3. ในฟิลด์ **ชื่อ** ป้อนชื่อข้อมูลลับของใบรับรองดิจิทัล สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)
4. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
5. ในฟิลด์ **ชนิด** เลือก **ใบรับรอง**
6. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="create-a-service-environment"></a>สร้างสภาพแวดล้อมบริการ

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
3. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมบริการ**
4. เลือก **สร้าง** เพื่อสร้างสภาพแวดล้อมบริการใหม่
5. ในฟิลด์ **ชื่อ** ป้อนชื่อของสภาพแวดล้อมการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
6. ในฟิลด์ **ข้อมูลลับของที่จัดเก็บโทเค็น SAS** ให้เลือกชื่อของความลับของบัญชีจัดเก็บที่ต้องใช้เพื่อตรวจสอบสิทธิ์ในการเข้าถึงบัญชีที่เก็บข้อมูล
7. ในส่วน **ผู้ใช้** ให้เลือก **เพิ่ม** เพื่อเพิ่มผู้ใช้ที่ได้รับอนุญาตให้ส่งใบแจ้งหนี้อิเล็กทรอนิกส์ผ่านสภาพแวดล้อม และเชื่อมต่อกับบัญชีการจัดเก็บด้วย
8. ในฟิลด์ **รหัสผู้ใช้** ให้ป้อนนามแฝงของผู้ใช้ ในฟิลด์ **อีเมล** ป้อนอยู่อีเมลของผู้ใช้
9. เลือก **บันทึก**
10. ถ้าใบแจ้งหนี้เฉพาะประเทศ/ภูมิภาคของคุณ จำเป็นต้องมีกลุ่มของใบรับรองเพื่อใช้ลายเซ็นดิจิทัล บนบานหน้าต่างการดำเนินการ เลือก **พารามิเตอร์ Key Vault** แล้วเลือก **กลุ่มของใบรับรอง** และทำตามขั้นตอนเหล่านี้:

    1. เลือก **สร้าง** เพื่อสร้างกลุ่มของใบรับรอง
    2. ในฟิลด์ **ชื่อ** ป้อนชื่อของกลุ่มของใบรับรอง ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
    3. ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองให้กับกลุ่ม
    4. ใช้ปุ่ม **ขึ้น** หรือ **ลง** เพื่อเปลี่ยนตําแหน่งของใบรับรองในกลุ่ม
    5. เลือก **ตกลง** และจากนั้นปิดหน้า
    6. ปิดหน้า

11. บนหน้า **สภาพแวดล้อมบริการ** บนบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** เพื่อเผยแพร่สภาพแวดล้อมไปยังระบบคลาวด์ ค่าของฟิลด์ **สถานะ** ถูกเปลี่ยนเป็น **เผยแพร่แล้ว**

## <a name="create-a-connected-application"></a>สร้างแอปพลิเคชันที่เชื่อมต่อ

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **แอปพลิเคชันที่เชื่อมต่อ**
2. เลือก **สร้าง** เพื่อสร้างแอปพลิเคชันที่เชื่อมต่อ
3. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อของแอปพลิเคชันที่จะเชื่อมต่อ
4. ในฟิลด์ **แอปพลิเคชัน** ให้ป้อน URL ของสภาพแวดล้อม Finance และ Supply Chain Management ที่จะเชื่อมต่อ
4. ในฟิลด์ **ผู้เช่า** ให้ป้อนผู้เช่าของสภาพแวดล้อม Finance และ Supply Chain Management
5. เลือก **บันทึก**
6. ในบานหน้าต่างการดำเนินการ ให้เลือก **ตรวจสอบการเชื่อมต่อ** เพื่อทดสอบการเชื่อมต่อกับสภาพแวดล้อม จากนั้น ปิดหน้า

## <a name="link-connected-applications-to-environments"></a>เชื่อมโยงแอปพลิเคชันที่เชื่อมต่อกับสภาพแวดล้อม

1. บนหน้า **การตั้งค่าสภาพแวดล้อม** ให้เลือก **สร้าง** เพื่อกําหนดแอปพลิเคชันที่เชื่อมต่อให้กับสภาพแวดล้อม
2. ในฟิลด์ **แอปพลิเคชันที่เชื่อมต่อ** ให้เลือกแอปพลิเคชันที่เชื่อมต่อ
3. ในฟิลด์ **สภาพแวดล้อมบริการ** เลือกสภาพแวดล้อมบริการ
4. เลือก **ตกลง** และจากนั้นปิดหน้า

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>ตั้งค่าการรวมการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance และ Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>เปิดคุณลักษณะการรวมของการออกใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้อินสแตนซ์ Finance หรือ Supply Chain Management ของคุณ
2. ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาคุณลักษณะ **การรวมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์** ถ้าคุณลักษณะนี้ไม่ปรากฏบนหน้า ให้เลือก **ตรวจสอบการอัปเดต**
3. เลือกคุณลักษณะ และจากนั้นเลือก **เปิดใช้งานตอนนี้**

### <a name="set-up-the-service-endpoint-url"></a>ตั้งค่า URL ปลายทางการบริการ

1. ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**
2. บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URL ปลายทาง** ให้ป้อนปลายทางของบริการที่เหมาะสมสำหรับภูมิศาสตร์ Azure ของคุณ ดังแสดงในตารางต่อไปนี้

    | ภูมิศาสตร์ของ Datacenter Azure | URI ปลายทางของบริการ                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | สหรัฐ              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ยุโรป                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | สหราชอาณาจักร             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | เอเชีย                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. ในฟิลด์ **สภาพแวดล้อม** ป้อนชื่อของสภาพแวดล้อมบริการที่เผยแพร่ในการออกใบแจ้งหนี้อิเล็กทรอนิกส์
4. เลือก **ตกลง** และจากนั้นปิดหน้า

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>เปิดใช้งานคีย์การสลับสำหรับ Finance หรือ Supply Chain Management รุ่น 10.0.17

1. ดำเนินการคำสั่ง SQL ต่อไปนี้:

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. ปฏิบัติการตามคำสั่ง IISreset สำหรับ AOS ทั้งหมด

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
