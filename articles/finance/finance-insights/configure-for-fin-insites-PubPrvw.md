---
title: การตั้งค่าคอนฟิกสำหรับ Finance Insights - รุ่น 10.0.20 และที่ใหม่กว่า
description: บทความนี้จะอธิบายการตั้งค่าคอนฟิกระบบของคุณเพื่อใช้ความสามารถที่มีอยู่ใน Finance insights รุ่น 10.0.20 และรุ่นที่ใหม่กว่า
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e6b9c34ee68a25ac9613a65cf63443751a39c576
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868531"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>การตั้งค่าคอนฟิกสำหรับ Finance Insights - รุ่น 10.0.20 และที่ใหม่กว่า

[!include [banner](../includes/banner.md)]



Finance Insights รวมฟังก์ชันจาก Microsoft Dynamics 365 Finance ที่มี Dataverse, Azure และ AI Builder เพื่อให้เครื่องมือการคาดการณ์ที่มีประสิทธิภาพสำหรับองค์กรของคุณ บทความนี้จะอธิบายการตั้งค่าคอนฟิก Dynamics 365 Finance รุ่น 10.0.20 เพื่อให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ใน Finance insights

> [!NOTE]
> ขั้นตอนการตั้งค่าคอนฟิกที่อธิบายไว้ในบทความนี้จะใช้เฉพาะกับ Finance รุ่น 10.0.20 และรุ่นที่ใหม่กว่าเท่านั้น หากต้องการตั้งค่า Finance Insights รุ่น 10.0.19 และเก่ากว่า ให้ดูที่ [การตั้งค่าคอนฟิกของ Finance insights - รุ่นสูงสุด 10.0.19](configure-for-fin-insites.md)

## <a name="deploy-finance"></a>ปรับใช้ Finance

ให้ทำตามขั้นตอนเหล่านี้เพื่อปรับใช้สภาพแวดล้อม

1. ใน Microsoft Dynamics Lifecycle Services (LCS) สร้างหรืออัปเดตข้อมูลสภาพแวดล้อม Finance สภาพแวดล้อมต้องการแอปการเงินและการดำเนินงาน รุ่น 10.0.20 หรือสูงกว่า
2. สภาพแวดล้อมต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูง (HA) ใน Sandbox (สภาพแวดล้อมชนิดนี้เรียกอีกอย่างว่า สภาพแวดล้อมระดับ 2) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
3. ถ้าคุณกําหนดค่าการเงินให้กับ Finance Insights ในสภาพแวดล้อม Sandbox คุณอาจต้องคัดลอกข้อมูลการผลิตไปยังสภาพแวดล้อมนั้นเพื่อให้การคาดการณ์สามารถทำงานได้ แบบจำลองการคาดการณ์จะใช้ข้อมูลหลายปีเพื่อสร้างการคาดการณ์ ข้อมูลสาธิต Contoso มีข้อมูลในอดีตไม่เพียงพอที่จะจัดการฝึกอบรมแบบจำลองการคาดการณ์อย่างเหมาะสม 

## <a name="configure-dataverse"></a>ตั้งค่าคอนฟิก Dataverse

ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิก Dataverse สำหรับ Finance Insights

1. ใน LCS เปิดหน้าสภาพแวดล้อมและตรวจสอบว่าส่วน **การรวม Power Platform** ได้รับการตั้งค่าเรียบร้อยแล้ว

    - ถ้ามีการตั้งค่าไว้แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Finance
    - ถ้าไม่มีการตั้งค่า ให้ทำตามขั้นตอนต่อไปนี้:

        1. ในส่วน **การรวม Power Platform** เลือก **การตั้งค่า** การตั้งค่าสภาพแวดล้อมอาจใช้เวลาถึงหนึ่งชั่วโมง
        2. ถ้ามีการตั้งค่าสภาพแวดล้อม Dataverse ไว้เสร็จสมบูรณ์แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Finance

        > [!NOTE]
        > เมื่อคุณเสร็จสิ้นการตั้งค่าสภาพแวดล้อมแล้ว **อย่า** เลือก **ลิงก์ไปยัง CDS สำหรับแอป** ปุ่มนี้ไม่เป็นปุ่มที่ไม่ต้องการสำหรับ Finance Insights หากคุณเลือก Add-in ของสภาพแวดล้อมที่กําหนดใน LCS คุณจะไม่สามารถตั้งค่าคอนฟิก Add-in ของสภาพแวดล้อมที่กําหนดได้

## <a name="configure-azure"></a>ตั้งค่าคอนฟิก Azure

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>ใช้ Azure Cloud Shell เพื่อตั้งค่าทรัพยากร Data Lake ของ Finance Insights

# <a name="use-a-windows-powershell-script"></a>[ใช้สคริปต์ Windows PowerShell](#tab/use-a-powershell-script)

มีการให้สคริปต์ Windows PowerShell ไว้ เพื่อให้คุณสามารถตั้งค่าทรัพยากร Azure ที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการส่งออกไปยัง Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ได้อย่างง่ายดาย ถ้าคุณต้องการดำเนินการตั้งค่าด้วยตนเอง ให้ข้ามกระบวนงานนี้ และดำเนินการต่อด้วยกระบวนงานในส่วน [การตั้งค่าด้วยตนเอง](#manual-setup) แทน

> [!NOTE]
> ใช้ขั้นตอนต่อไปนี้เพื่อเรียกใช้สคริปต์ Windows PowerShell การตั้งค่าอาจใช้ไม่ได้ หากคุณใช้ตัวเลือก **ทดลองใช้** ใน Azure CLI หรือหากคุณเรียกใช้สคริปต์บนคอมพิวเตอร์ของคุณ

ทำตามขั้นตอนต่อไปนี้โดยใช้สคริปต์ Windows PowerShell เพื่อตั้งค่าคอนฟิก Azure คุณต้องมีสิทธิ์ในการสร้างกลุ่มทรัพยากร Azure ทรัพยากร Azure และแอปพลิเคชัน Azure AD สำหรับข้อมูลเกี่ยวกับสิทธิ์ที่จำเป็น ให้ดูที่ [ตรวจสอบสิทธิ์ Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)

1. ใน [พอร์ทัล azure](https://portal.azure.com) ให้ไปที่การบอกรับเป็นสมาชิก Azure เป้าหมายของคุณ
2. เลือก **Cloud Shell** ทางด้านขวาของฟิลด์ **ค้นหา**
3. เลือก **PowerShell**
4. สร้างที่เก็บข้อมูล ถ้าคุณได้รับพร้อมท์ให้สร้าง
5. บนแท็บ **Azure CLI** เลือก **คัดลอก**
6. ใน Notepad ให้เปิดไฟล์ใหม่และวางในสคริปต์ Windows PowerShell
7. บันทึกไฟล์เป็น **ConfigureDataLake.ps1**
8. อัพโหลดสคริปต์ Windows PowerShell ไปยังรอบเวลาโดยใช้ตัวเลือกเมนูเพื่ออัพโหลดใน Cloud Shell
9. เรียกใช้สคริปต์ **.\ConfigureDataLake.ps1**
10. ติดตามพร้อมท์เพื่อเรียกใช้สคริปต์
11. ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อติดตั้ง add-in ส่งออกไปยัง Data Lake ใน LCS

### <a name="manual-setup"></a>การตั้งค่าด้วยตนเอง

#### <a name="add-applications-to-the-azure-ad-tenant"></a>เพิ่มแอปพลิเคชันในผู้เช่า Azure AD

1. ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory**
2. เลือก **จัดการ \> แอปพลิเคชันองค์กร**
3. ค้นหาแอปพลิเคชันต่อไปนี้ตามรหัสของแอป

    | ใบคำขอเปิด                              | รหัสแอป                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | บริการตรวจสอบ AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

ถ้าคุณไม่พบแอปพลิเคชันก่อนหน้าใดๆ ให้ลองทำตามขั้นตอนต่อไปนี้

1. บนคอมพิวเตอร์เฉพาะที่ของคุณ ให้เลือกเมนู **เริ่มต้น** ค้นหา **powershell**
2. เลือกและกดค้างไว้ (หรือคลิกขวา) **Windows PowerShell** และจากนั้น เลือก **เรียกใช้ในฐานะผู้ดูแลระบบ**
3. เรียกใช้คำสั่งต่อไปนี้เพื่อติดตั้งโมดูล **AzureAD**

    `Install-Module -Name AzureAD`

4. ถ้าต้องการให้ผู้ให้บริการ NuGet ดำเนินการต่อ ให้เลือก **Y** เพื่อติดตั้ง
5. ถ้าคุณได้รับข้อความ "ที่เก็บที่ไม่น่าเชื่อถือ" ให้เลือก **Y** เพื่อดำเนินการต่อ
6. สำหรับแต่ละแอปพลิเคชันที่ต้องมีการเพิ่ม ให้เรียกใช้คำสั่งต่อไปนี้เพื่อเพิ่มแอปพลิเคชันไปยัง Azure AD เมื่อคุณได้รับพร้อมท์ ให้ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบ Azure AD

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>สร้างแหล่งข้อมูล Azure

> [!NOTE]
> ตรวจสอบให้แน่ใจว่าคุณได้สร้างทรัพยากรต่อไปนี้ในอินสแตนซ์ Azure AD ที่เหมือนกันกับสภาพแวดล้อม Dataverse คุณไม่สามารถใช้ทรัพยากรจากอินสแตนซ์ Azure AD อื่นได้

1. การสร้างบัญชีที่จัดเก็บ:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้างบัญชีที่จัดเก็บ
    2. ในกล่องโต้ตอบ **สร้างบัญชีที่จัดเก็บ** ให้ตั้งค่าฟิลด์ต่อไปนี้:

        - **สถานที่** – เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ
        - **ประสิทธิภาพ** – เราขอแนะนำให้คุณเลือก **มาตรฐาน**
        - **ชนิดบัญชี** – คุณต้องเลือก **StorageV2**

    3. ในกล่องโต้ตอบ **ตัวเลือกขั้นสูง** สำหรับตัวเลือก **Data Lake storage Gen2** เลือก **เปิดใช้งาน** ภายใต้คุณลักษณะ **namespaces ตามลำดับชั้น** ถ้าคุณไม่เปิดใช้งานคุณลักษณะนี้ คุณไม่สามารถใช้ข้อมูลที่แอปการเงินและการดำเนินงานเขียนโดยใช้บริการต่างๆ เช่น โฟลว์ข้อมูล Power BI
    4. เลือก **รีวิวและสร้าง** เมื่อการปรับใช้งานเสร็จสมบูรณ์ จะมีการแสดงทรัพยากรใหม่ในพอร์ทัล Azure
    5. ไปที่บัญชีจัดเก็บข้อมูลที่คุณสร้างขึ้น
    6. บนเมนูด้านซ้าย ให้เลือก **คีย์การเข้าถึง**
    7. คัดลอกและบันทึกชื่อบัญชีที่จัดเก็บ คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault

2. สร้าง Key Vault:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้าง Key Vault
    2. ในกล่องโต้ตอบ **สร้าง Key Vault** ในฟิลด์ **สถานที่** ให้เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ
    3. หลังจากที่สร้าง key vault แล้ว ให้ไปที่ **ภาพรวม Key Vault** และคัดลอกและบันทึกชื่อ DNS คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่า add-in ของ Data Lake

3. สร้างและลงทะเบียนแอปพลิเคชัน Azure AD:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory** แล้วจากนั้น เลือก **การลงทะเบียนแอป**
    2. เลือก **การลงทะเบียนแอปพลิเคชันใหม่** และตั้งค่าฟิลด์ต่อไปนี้:

        - **ชื่อ** – ป้อนชื่อของแอป
        - **ชนิดของแอปพลิเคชัน** – เลือก **Web API**
        - **เปลี่ยนเส้นทางการตั้งค่า URI** – ป้อน URL สำหรับอินสแตนซ์ Dynamics 365 ของคุณ เช่น `https://yourdynamicsinstance.dynamics.com/auth`

    3. ไปที่แอปพลิเคชันที่คุณเพิ่งสร้างขึ้น และคัดลอกและบันทึกค่า **รหัสของแอปพลิเคชัน (ไคลเอนต์)** คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault
    4. ไปที่ **สิทธิ์ของ API** และปฏิบัติตามขั้นตอนเหล่านี้:

        1. เลือก **เพิ่มสิทธิ์**
        2. เลือก **Azure Key Vault**
        3. หลังจากที่คุณเลือกสิทธิ์ที่ได้รับมอบหมาย ให้เลือก **ผู้ใช้\_การเลียนแบบ**
        4. เลือก **เพิ่มสิทธิ์**

    5. บนเมนูสำหรับแอป ให้เลือก **ใบรับรอง \& ข้อมูลลับ** และจากนั้น ทำตามขั้นตอนต่อไปนี้เพื่อสร้างข้อมูลลับของ Key Vault:

        1. เลือก **ข้อมูลลับของไคลเอนต์ใหม่**
        2. ในฟิลด์ **คำอธิบาย Key** ให้ป้อนชื่อ
        3. เลือกระยะเวลา แล้วจากนั้น เลือก **เพิ่ม** ข้อมูลลับจะถูกสร้างขึ้นในฟิลด์ **ค่า**
        4. คัดลอกและบันทึกค่าข้อมูลลับไคลเอนต์ คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault

4. สร้างข้อมูลลับของ Key Vault:

    1. ไปที่ Key Vault ที่คุณสร้างไว้ก่อนหน้านี้ และเลือก **ข้อมูลลับ**
    2. สำหรับชื่อลับแต่ละชื่อในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือก **สร้าง/นำเข้า**
        2. ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**
        3. สร้างชื่อและค่าลับจากตาราง
        4. เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง** ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault

        | ชื่อข้อมูลลับ                       | ค่าลับ                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | รหัสแอป                            | รหัสแอปของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้                                      |
        | ข้อมูลลับของแอป                        | ข้อมูลลับของไคลเอนต์ที่คุณบันทึกไว้ก่อนหน้านี้                                                    |
        | ชื่อบัญชีที่จัดเก็บ              | ชื่อของบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้ เช่น **storageaccount1**       |

5. อนุญาตให้แอปพลิเคชันเข้าถึง key vault:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิด key vault ที่คุณสร้างไว้ก่อนหน้านี้
    2. เลือกนโยบายการเข้าถึง
    3. สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือก **เพิ่มนโยบายการเข้าถึง** เพื่อสร้างนโยบายการเข้าถึง
        2. ในฟิลด์ **สิทธิ์ของข้อมูลลับ** ให้เลือกสิทธิ์จากตาราง
        3. ในฟิลด์ **หลักการเลือก** ให้ค้นหาชื่อที่แสดงของแอปพลิเคชันจากตาราง
        4. เลือก **เลือก**
        5. เลือก **เพิ่ม**
        6. เลือก **บันทึก**

        | ใบคำขอเปิด                                              | สิทธิ์ |
        |----------------------------------------------------------|-------------|
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เรียกดู รายการ   |
        | **Microsoft Dynamics ERP Microservices**                 | เรียกดู รายการ   |

6. กำหนดบทบาทที่จะเข้าถึงบัญชีที่จัดเก็บ:

    1. ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิดบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้
    2. เลือก **การควบคุมการเข้าถึง (IAM)** และจากนั้น เลือก **การกำหนดบทบาท**
    3. เลือก **เพิ่ม เพิ่มการกำหนดบทบาท**
    4. สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:

        1. เลือกบทบาทจากตาราง
        2. ปล่อยฟิลด์ **กำหนดการเข้าถึงแก่** ให้มีการตั้งค่าเป็น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**
        3. ในฟิลด์ **เลือก** ให้ป้อนแอปพลิเคชันจากตาราง
        4. เลือก **บันทึก**

        | ใบคำขอเปิด                                              | บทบาท                        |
        |----------------------------------------------------------|-----------------------------|
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เจ้าของ                       |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | ผู้จ่ายสมทบ                 |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | ผู้สนับสนุนบัญชีที่จัดเก็บ |
        | ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง | เจ้าของข้อมูล Blob ที่จัดเก็บ     |
        | **บริการตรวจสอบ AI Builder**                     | ตัวอ่านข้อมูล Blob ที่จัดเก็บ    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a>ตั้งค่าคอนฟิกการส่งออกไปยัง add-in ของ Data Lake

ทำตามขั้นตอนต่อไปนี้เพื่อใช้ LCS เพื่อเพิ่มการส่งออกไปยัง add-in ของ Data Lake ไปยังสภาพแวดล้อม

1. ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**
2. ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**
3. เลือก add-in **ส่งออกไปยัง Data Lake**
4. ป้อนค่าต่อไปนี้

    | มูลค่า                                                              | คำอธิบาย |
    |--------------------------------------------------------------------|-------------|
    | รหัสผู้เช่าของการบอกรับเป็นสมาชิก Azure ที่เป็นที่ตั้งของ Key Vault | รหัสผู้เช่าซึ่งเป็นที่ตั้งของบัญชีที่จัดเก็บ แอป และ Key Vault หากต้องการได้รับค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า** |
    | ระบุชื่อ DNS ของ Key Vault ของคุณ                             | ชื่อ DNS ของ Key Vault เช่น `https://customkeyvault.vault.azure.net/` |
    | ระบุข้อมูลลับที่มีชื่อของบัญชีที่จัดเก็บ   | **ชื่อ-บัญชี-ที่จัดเก็บ** |
    | ชื่อลับสำหรับรหัสแอปที่จะใช้สำหรับการเข้าถึง Data Lake          | **รหัส-แอป** |
    | ชื่อข้อมูลลับของข้อมูลลับไคลเอนต์แอป                                  | **ข้อมูลลับ-แอป** |

5. ยอมรับเงื่อนไข และเลือกจากนั้น **ติดตั้ง**

จะมีการติดตั้ง add-in ภายในสองสามนาที

## <a name="configure-the-finance-insights-add-in"></a>ตั้งค่าคอนฟิก add-in ของ Finance Insights

> [!NOTE]
> ถ้าคุณติดตั้ง Add-in ของรับข้อมูลเชิงลึกไว้ก่อนหน้านี้ ให้ถอนการติดตั้งก่อนที่คุณจะสามารถปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อติดตั้ง Add-in ของ Finance Insights

1. ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**
2. ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**
3. เลือก add-in ของ **Finance Insights**
4. ยอมรับเงื่อนไข และเลือกจากนั้น **ติดตั้ง**

Add-in อาจใช้เวลาหลายนาทีในการติดตั้ง

## <a name="feedback-and-support"></a>ผลป้อนกลับและการสนับสนุน

หากคุณมีความสนใจในการให้ผลป้อนกลับ หรือหากคุณต้องการความช่วยเหลือ โปรดส่งอีเมลถึง [Finance insights](mailto:fiap@microsoft.com)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
