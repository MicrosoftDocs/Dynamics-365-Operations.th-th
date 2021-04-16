---
title: Add-in การมองเห็นสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิกAdd-in การมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e294ada8dd3e764987aa363adb2614416986575b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821140"
---
# <a name="inventory-visibility-add-in"></a>Add-in การมองเห็นสินค้าคงคลัง

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Add-in การมองเห็นสินค้าคงคลังเป็น microservice อิสระและปรับสเกลได้อย่างมาก ซึ่งเปิดใช้งานการติดตามปริมาณคงคลังคงเหลือในเวลาจริง จึงให้มุมมองส่วนกลางของการมองเห็นสินค้าคงคลัง

ข้อมูลทั้งหมดที่เกี่ยวข้องกับปริมาณคงคลังคงเหลือจะถูกส่งออกไปยังบริการใกล้เคียงเวลาจริงผ่านการรวม SQL ในระดับต่ำ ระบบภายนอกเข้าถึงบริการผ่าน RESTful APIs เพื่อสอบถามข้อมูลปริมาณคงคลังคงเหลือในชุดของมิติที่กำหนด ดังนั้นจึงดึงข้อมูลรายการของตำแหน่งในปริมาณคงคลังคงเหลือที่พร้อมใช้งาน

การแสดงผลสินค้าคงคลังเป็น microservice ที่สร้างขึ้นบน Microsoft Dataverse ซึ่งหมายความว่า คุณสามารถขยายได้โดยการสร้าง Power Apps และการใช้ Power BI เพื่อให้ฟังก์ชันการทำงานที่กำหนดเองตรงกับความต้องการทางธุรกิจของคุณ นอกจากนี้ คุณยังสามารถอัปเกรดดัชนีเพื่อทำการสอบถามสินค้าคงคลังได้ด้วย

ความสามารถในการมองเห็นสินค้าคงคลังจะให้ตัวเลือกการตั้งค่าคอนฟิกซึ่งช่วยให้สามารถรวมกับระบบต่างๆ ของบุคคลที่สามได้ ซึ่งสนับสนุนมิติสินค้าคงคลังมาตรฐาน ความสามารถที่กำหนดเอง และปริมาณที่มีการคำนวณซึ่งสามารถตั้งค่าคอนฟิกได้แบบมาตรฐาน

หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิก Add-in ความสามารถในการมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management และวิธีใช้ Application Programming Interface (API)

## <a name="install-the-inventory-visibility-add-in"></a>ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง

คุณจำเป็นต้องติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลังโดยใช้ Microsoft Dynamics Lifecycle Services (LCS) LCS เป็นพอร์ทัลการทำงานร่วมกันที่ให้สภาพแวดล้อมและชุดของบริการที่อัปเดตเป็นประจำ ซึ่งช่วยให้คุณสามารถจัดการวงจรการใช้งานแอปพลิเคชันของแอป Dynamics 365 Finance and Operations ของคุณได้

สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะสามารถติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง คุณต้องดำเนินการขั้นตอนต่อไปนี้:

- รับโครงการสำหรับการใช้งาน LCS โดยมีสภาพแวดล้อมที่ปรับใช้อย่างน้อยหนึ่งรายการ
- โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่า Add-in ของข้อกำหนดเบื้องต้น ใน [ภาพรวมของ Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) เสร็จเรียบร้อยแล้ว Inventory Visibility ไม่ต้องการการเชื่อมโยงแบบสองทิศทาง
- ติดต่อ Inventory Visibility Team ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์ที่ต้องการสามไฟล์ต่อไปนี้:

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - `Inventory Visibility Integration.zip` (ถ้าเวอร์ชันของ Supply Chain Management ที่คุณรันอยู่เป็นรุ่นก่อนหน้าเวอร์ชัน 10.0.18)

> [!NOTE]
> ประเทศและภูมิภาคที่ได้รับการสนับสนุนในปัจจุบัน ได้แก่ แคนาดา สหรัฐอเมริกา และสหภาพยุโรป (EU)

ถ้าคุณมีคำถามใดๆ เกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ โปรดติดต่อทีมงานผลิตภัณฑ์ของความสามารถในการมองเห็นสินค้าคงคลัง

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>ตั้งค่า Dataverse

ให้ดำเนินการตามขั้นตอนต่อไปนี้เพื่อตั้งค่า Dataverse

1. เพิ่มหลักการบริการให้กับผู้เช่าของคุณ:

    1. ติดตั้ง Azure AD PowerShell Module v2 ตามที่อธิบายไว้ใน [ติดตั้ง Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2)
    1. โดยรันคำสั่ง PowerShell ต่อไปนี้:

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. สร้างผู้ใช้แอพลิเคชัน สำหรับ Inventory Visibility ใน Dataverse:

    1. เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ
    1. ไปที่ **การตั้งค่าขั้นสูง \> ระบบ \> ความปลอดภัย \> ผู้ใช้** และสร้างผู้ใช้แอพลิเคชัน ใช้เมนูมุมมองเพื่อเปลี่ยนมุมมองหน้าเป็น **ผู้ใช้แอพลิเคชัน**
    1. เลือก **ใหม่** ตั้งค่ารหัสแอพลิเคชัน เป็น *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* (รหัสออบเจ็กต์จะถูกโหลดโดยอัตโนมัติเมื่อคุณบันทึกการเปลี่ยนแปลง) คุณสามารถปรับแต่งชื่อได้ ตัวอย่างเช่น คุณสามารถเปลี่ยนเป็น *Inventory Visibility* เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **บันทึก**
    1. เลือก **กําหนดบทบาท** แล้วเลือก **ผู้ดูแลระบบ** ถ้ามีบทบาทที่มีชื่อ **ผู้ใช้ Common Data Service** ให้เลือกบทบาทนั้นด้วย

    สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผู้ใช้แอพลิเคชัน](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)

1. นําเข้าไฟล์ `Inventory Visibility Dataverse Solution.zip` ซึ่งประกอบด้วย เอนทิตี้ที่เกี่ยวข้องกับการตั้งค่าคอนฟิก Dataverse และ Power Apps

    1. ไปที่หน้า **โซลูชัน**
    1. เลือก **นำเข้า**

1. นําเข้าโฟลว์ทริกเกอร์การอัปเกรดการตั้งค่าคอนฟิก:

    1. ไปที่หน้า Microsoft Flow
    1. ตรวจสอบให้แน่ใจว่ามีการเชื่อมต่อที่ชื่อ *Dataverse (ดั้งเดิม)* อยู่ (ถ้าไม่มี ให้สร้างใหม่)
    1. นำเข้าไฟล์ `Inventory Visibility Configuration Trigger.zip` หลังจากนําเข้าแล้ว ทริกเกอร์จะปรากฏขึ้นภายใต้ **โฟลว์ของฉัน**
    1. เริ่มต้นตัวแปรสี่ตัวต่อไปนี้ ตามข้อมูลสภาพแวดล้อม:

        - รหัสผู้เช่า Azure
        - รหัสไคลเอนต์แอปพลิเคชัน Azure
        - ข้อมูลลับไคลเอนต์แอปพลิเคชัน Azure
        - ปลายทางการแสดงผลสินค้าคงคลัง

            สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรนี้ โปรดดูที่ส่วน [ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง](#setup-inventory-visibility-integration) ในตอนท้ายของหัวข้อนี้

        ![ทริกเกอร์การตั้งค่าคอนฟิก](media/configuration-trigger.png "ทริกเกอร์การตั้งค่าคอนฟิก")

    1. เลือก **เปิด**

### <a name="install-the-add-in"></a><a name="install-add-in"></a>ติดตั้ง Add-in

เพื่อติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง ต้องดำเนินการขั้นตอนต่อไปนี้:

1. ลงชื่อเข้าใช้พอร์ทัล [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)
1. บนโฮมเพจ ให้เลือกโครงการที่มีการปรับใช้สภาพแวดล้อมของคุณ
1. บนหน้าโครงการ ให้เลือกสภาพแวดล้อมที่คุณต้องการติดตั้ง add-in
1. ในหน้าสภาพแวดล้อม ให้เลื่อนลงจนกว่าคุณจะเห็นส่วน **Add-in ของสภาพแวดล้อม** ในส่วน **Power Platform การรวม** ที่คุณสามารถค้นหาชื่อสภาพแวดล้อม Dataverse ได้
1. ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**

    ![หน้าสภาพแวดล้อมใน LCS](media/inventory-visibility-environment.png "หน้าสภาพแวดล้อมใน LCS")

1. เลือกลิงก์ **ติดตั้ง Add-in ใหม่** รายการของ add-in ที่พร้อมใช้งานจะเปิดขึ้น
1. เลือก **การแสดงผลสินค้าคงคลัง** ในรายการ
1. ป้อนค่าสำหรับฟิลด์ต่อไปนี้สำหรับสภาพแวดล้อมของคุณ:

    - **รหัส (ไคลเอนต์) แอปพลิเคชัน AAD**
    - **รหัสผู้เช่า AAD**

    ![หน้าการตั้งค่าของ Add in](media/inventory-visibility-setup.png "หน้าการตั้งค่าของ Add in")

1. ยอมรับข้อกำหนดและเงื่อนไขโดยเลือกกล่องกาเครื่องหมาย **ข้อกำหนดและเงื่อนไข**
1. เลือก **ติดตั้ง** สถานะของ add-in จะแสดงเป็น **กำลังติดตั้ง** เมื่อเสร็จสิ้นแล้ว ให้รีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงสถานะเป็น **ติดตั้งแล้ว**

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>ถอนการติดตั้ง Add-in

เมื่อต้องการถอนการติดตั้ง add-in ให้เลือก **ถอนการติดตั้ง** เมื่อคุณรีเฟรช LCS และ Add-in การแสดงผลสินค้าคงคลังจะถูกลบออก กระบวนการถอนการติดตั้งจะลบการลงทะเบียน Add-in และยังเริ่มต้นงานเพื่อล้างข้อมูลทางธุรกิจทั้งหมดที่จัดเก็บไว้ในบริการด้วย

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>ใช้ข้อมูลปริมาณคงคลังคงเหลือจาก Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>ปรับใช้แพคเกจการรวมการแสดงผลสินค้าคงคลัง

ถ้าคุณรัน Supply Chain Management เวอร์ชัน 10.0.17 หรือก่อนหน้านั้น ให้ติดต่อทีมสนับสนุนการแสดงผลสินค้าคงคลัง ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์แพคเกจ แล้วปรับใช้แพคเกจใน LCS

> [!NOTE]
> ถ้าเกิดข้อผิดพลาดที่ไม่ตรงกันของเวอร์ชันระหว่างการปรับใช้ คุณต้องนําเข้าโครงการ X++ ด้วยตนเอง ลงในสภาพแวดล้อมการพัฒนาของคุณ จากนั้นสร้างแพคเกจที่สามารถปรับใช้งานได้ในสภาพแวดล้อมการพัฒนาของคุณ และปรับใช้ในสภาพแวดล้อมการทำงานจริงของคุณ
> 
> รหัสถูกรวมอยู่กับ Supply Chain Management เวอร์ชัน 10.0.18 ถ้าคุณรันเวอร์ชันนั้นอยู่หรือเวอร์ชันที่ใหม่กว่า ไม่ต้องมีการปรับใช้

ตรวจสอบให้แน่ใจว่าคุณลักษณะต่อไปนี้ได้เปิดใช้งานอยู่ในสภาพแวดล้อม Supply Chain Management ของคุณ (โดยค่าเริ่มต้น จะเปิดใช้งาน)

| คำอธิบายลักษณะการทำงาน | เวอร์ชันรหัส | สลับคลาส |
|---|---|---|
| เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSum | 10.0.11 | InventUseDimOfInventSumToggle |
| เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง

1. ใน Supply Chain Management ให้เปิดพื้นที่ทำงาน **[การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** และเปิดคุณลักษณะ **การรวมการแสดงผลสินค้าคงคลัง**
1. ไปที่ **การจัดการสินค้าคงคลัง \> ตั้งค่า \> พารามิเตอร์การรวมการแสดงผลสินค้าคงคลัง** และป้อน URL ของสภาพแวดล้อมที่คุณรันการแสดงผลสินค้าคงคลังอยู่

    ค้นหาภูมิภาค Azure ของสภาพแวดล้อม LCS ของคุณ แล้วป้อน URL URL มีฟอร์มต่อไปนี้:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    ตัวอย่างเช่น ถ้าคุณอยู่ในยุโรป สภาพแวดล้อมของคุณจะมี URL อย่างใดอย่างหนึ่งต่อไปนี้:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    ภูมิภาคต่อไปนี้พร้อมใช้งานในขณะนี้

    | ภูมิภาคของ Azure | ชื่อย่อของภูมิภาค |
    |---|---|
    | ออสเตรเลียตะวันออก | eau |
    | ออสเตรเลียตะวันออกเฉียงใต้ | seau |
    | แคนาดากลาง | cca |
    | แคนาดาตะวันออก | eca |
    | ยุโรปเหนือ | neu |
    | ยุโรปตะวันตก | weu |
    | สหรัฐอเมริกาตะวันออก | eus |
    | สหรัฐอเมริกาตะวันตก | wus |

1. ไปที่ **การจัดการสินค้าคงคลัง \> ประจำงวด \> การรวมการแสดงผลสินค้าคงคลัง** และเปิดใช้งานงาน ขณะนี้เหตุการณ์การเปลี่ยนแปลงสินค้าคงคลังทั้งหมดจาก Supply Chain Management จะถูกลงรายการบัญชีไปยังการแสดงผลสินค้าคงคลัง

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง

REST API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง แสดงถึงปลายทางเฉพาะสำหรับการรวมหลายแห่ง ซึ่งสนับสนุนชนิดการโต้ตอบหลักสามชนิด:

- การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก
- การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก
- การซิงโครไนส์อัตโนมัติกับ Supply Chain Management สินค้าคงคลังคงเหลือ

การซิงโครไนส์อัตโนมัติไม่ได้เป็นส่วนหนึ่งของ API สาธารณะ แต่จะถูกจัดการในพื้นหลังของสภาพแวดล้อมซึ่งเปิดใช้งาน Add-in ของการแสดงผลสินค้าคงคลัง

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>การรับรองความถูกต้อง

โทเคนความปลอดภัยของแพลตฟอร์มจะใช้ในการเรียก Add-in ของการแสดงผลสินค้าคงคลัง ดังนั้น คุณจึงต้องสร้างโทเคน *Azure Active Directory (Azure AD)* โดยใช้แอพลิเคชัน Azure AD ของคุณ จากนั้นคุณต้องใช้โทเคน Azure AD เพื่อรับ *การเข้าถึงโทเคน* จากบริการความปลอดภัย

รับโทเคนบริการรักษาความปลอดภัย โดยทำตามขั้นตอนต่อไปนี้:

1. ล็อกอินเข้าสู่พอร์ทัล Azure และใช้งาน เพื่อค้นหา `clientId` และ `clientSecret` สำหรับแอพลิเคชัน Supply Chain Management ของคุณ
1. การดึงข้อมูลโทเค็น Azure Active Directory (`aadToken`) โดยการส่งการร้องขอ HTTP มีคุณสมบัติต่อไปนี้:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **วิธีการ** - `GET`
    - **ตัวเนื้อหา (ข้อมูลแบบฟอร์ม)**:

        | คีย์ | ค่า |
        | --- | --- |
        | รหัส_ไคลเอนต์ | ${aadAppId} |
        | ข้อมูลลับ_ไคลเอ็นต์ | ${aadAppSecret} |
        | ชนิด_การให้สิทธิ์ | ข้อมูลประจำตัว_ไคลเอ็นต์ |
        | ทรัพยากร | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. คุณควรได้รับ `aadToken` ในการตอบสนอง ซึ่งคล้ายกับตัวอย่างต่อไปนี้

    ```json
    {
    "token_type": "Bearer",
    "expires_in": "3599",
    "ext_expires_in": "3599",
    "expires_on": "1610466645",
    "not_before": "1610462745",
    "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
    "access_token": "eyJ0eX...8WQ"
    }
    ```

1. สร้างการร้องขอ JSON ที่คล้ายกับสิ่งต่อไปนี้

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    ที่ใด:
    - ค่า `client_assertion` ต้องเป็น `aadToken` ที่คุณได้รับในขั้นตอนก่อนหน้านี้
    - ค่า `context` ต้องเป็นรหัสสภาพแวดล้อมที่คุณต้องการปรับใช้ Add-in
    - ตั้งค่าอื่นๆ ทั้งหมด ตามที่แสดงในตัวอย่าง

1. ส่งการร้องขอ HTTP ที่มีคุณสมบัติต่อไปนี้:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **วิธีการ** - `POST`
    - **ส่วนหัว HTTP** - รวมถึงเวอร์ชันของ API (คีย์คือ `Api-Version` และค่าเป็น `1.0`)
    - **ตัวเนื้อหา** - รวมถึงการร้องขอ JSON ที่คุณสร้างในขั้นตอนก่อนหน้านี้

1. คุณจะได้รับ `access_token` ในการตอบสนอง นี่คือสิ่งที่คุณต้องการในฐานะโทเคนผู้ถือสิทธิ์เพื่อเรียก API ความสามารถในการมองเห็นสินค้าคงคลัง นี่คือตัวอย่าง

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>ตั้งค่าคอนฟิก API ความสามารถในการมองเห็นสินค้าคงคลัง

ก่อนที่จะใช้บริการ คุณต้องทำการตั้งค่าคอนฟิกที่อธิบายไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสมบูรณ์ การตั้งค่าคอนฟิกอาจแตกต่างกันไปตามรายละเอียดของสภาพแวดล้อมของคุณ ส่วนใหญ่แล้วประกอบด้วยสี่ส่วน:

- [การแบ่งพาร์ติชัน](#partitioning)
- [การตั้งค่าคอนฟิกมิติ](#dimension-configurations)
- [การจัดทำดัชนี](#indexing)
- [การวัดแบบกำหนดเอง](#custom-measurement)

#### <a name="partitioning"></a>การแบ่งพาร์ติชัน

การแบ่งพาร์ติชันสามารถมีผลกระทบต่อประสิทธิภาพการทำงานของ API ความสามารถในการมองเห็นสินค้าคงคลังได้อย่างมาก ขอแนะนำให้คุณกำหนดโครงร่างที่อนุญาตให้มีการจัดกลุ่มข้อมูลเล็กๆ ในขณะที่ยังคงอนุญาตให้มีการสอบถามข้อมูลที่มีความหมาย

`organizationId` (`dataAreaId` ใน Supply Chain Management) จะเป็นส่วนหนึ่งของการแบ่งพาร์ติชันเสมอ และตามค่าเริ่มต้น ความสามารถในการมองเห็นสินค้าคงคลังจะถูกตั้งค่าเป็นพาร์ติชันตามมิติเป็น *ไซต์ + สถานที่* นี่หมายความว่าบริการต้องมีการสอบถามเสมอด้วยมิติเหล่านี้ที่กำหนดไว้ในตัวกรอง

> [!NOTE]
> *ไซต์* และ *สถานที่* เป็นมิติเริ่มต้นทั่วไปสองมิติในความสามารถในการมองเห็นสินค้าคงคลัง ใน Supply Chain Management มิติเหล่านี้เรียกว่า *ไซต์* (`InventSiteId`) และ *คลังสินค้า* (`InventLocationId`)

### <a name="dimension-configurations"></a>การตั้งค่าคอนฟิกมิติ

ความสามารถในการมองเห็นสินค้าคงคลังจะแสดงรายการของมิติเริ่มต้นทั่วไป เพื่อเปิดใช้งานการรวมระบบแหล่งที่มาหลายรายการ

ตารางต่อไปนี้แสดงรายการมิติสินค้าคงคลังที่จะเป็นชื่อมิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง

| ชนิดมิติ | ชื่อมิติ |
|---|---|
| ผลิตภัณฑ์ | `ColorId` |
| ผลิตภัณฑ์ | `SizeId` |
| ผลิตภัณฑ์ | `StyleId` |
| ผลิตภัณฑ์ | `ConfigId` |
| การติดตาม | `BatchId` |
| การติดตาม | `SerialId` |
| ที่ตั้ง | `LocationId` |
| ที่ตั้ง | `SiteId` |
| สถานะของสินค้าคงคลัง | `StatusId` |
| คลังสินค้าเฉพาะ | `WMSLocationId` |
| คลังสินค้าเฉพาะ | `WMSPalletId` |
| คลังสินค้าเฉพาะ | `LicensePlateId` |

> [!NOTE]
> ชนิดของมิติที่แสดงรายการอยู่ในตารางก่อนหน้านี้ใช้สำหรับการอ้างอิงเท่านั้น คุณไม่จำเป็นต้องกำหนดชนิดมิติในความสามารถในการมองเห็นสินค้าคงคลัง

ถ้ามีมิติที่กำหนดเองอยู่และจำเป็นต้องโฟลว์ไปยังค่าเริ่มต้น เมื่อมีการใช้งานโดยความสามารถในการมองเห็นสินค้าคงคลัง คุณสามารถตั้งค่าคอนฟิก **ชื่อมิติที่กำหนดเอง** ในความสามารถในการมองเห็นสินค้าคงคลัง

ระบบภายนอกเข้าถึงความสามารถในการมองเห็นสินค้าคงคลังผ่าน RESTful APIs ที่เปิดใช้งานข้อมูลปริมาณคงคลังคงเหลือในชุดที่กำหนดของมิติที่จะมีการสอบถาม สำหรับการรวม ความสามารถในการมองเห็นสินค้าคงคลังจะช่วยให้คุณสามารถตั้งค่าคอนฟิก *แหล่งข้อมูลช่องทางภายนอก* และมิติแหล่งที่มาเป็น *มิติเป้าหมาย* ในความสามารถในการมองเห็นสินค้าคงคลัง

มิติเป้าหมายควรเป็นหนึ่งในรายการต่อไปนี้:

- มิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง
- มิติที่กำหนดเอง

วัตถุประสงค์ของการตั้งค่าคอนฟิกมิติคือ การกำหนดมาตรฐานการรวมหลายระบบสำหรับการสอบถามบนมิติและเหตุการณ์การโพสต์กับมิติ

#### <a name="indexing"></a>การจัดทำดัชนี

ส่วนใหญ่การสอบถามปริมาณคงคลังคงเหลือไม่เพียงแค่อยู่ที่ระดับ "ยอดรวม" สูงสุด แต่คุณอาจต้องการดูผลลัพธ์ที่รวมโดยยึดตามมิติสินค้าคงคลัง

ความสามารถในการมองเห็นสินค้าคงคลังให้ความยืดหยุ่นโดยการอนุญาตให้คุณตั้งค่าดัชนี ซึ่งขึ้นอยู่กับมิติหรือชุดของมิติ

> [!NOTE]
> ในขณะนี้ คุณสามารถตั้งค่าคอนฟิกดัชนีได้สูงสุดห้ารายการเท่านั้น คุณต้องคำนึงถึงมิติหรือชุดของมิติที่คุณจะใช้ก่อนที่จะดำเนินการ เพื่อให้มั่นใจว่าจะตอบสนองความต้องการทางธุรกิจของคุณ ตัวอย่างเช่น ถ้าคุณต้องการสอบถามผลิตภัณฑ์ดังต่อไปนี้:

- สอบถามปริมาณคงคลังคงเหลือของผลิตภัณฑ์แบบรวมตามมิติ *สี* และ *ขนาด*
- ในบางกรณี คุณต้องการสอบถามเกี่ยวกับผลิตภัณฑ์โดยรวมเท่านั้น

คุณจะกำหนดดัชนีสองรายการดังต่อไปนี้:

- `["ColorId", "SizeId"]`
- `[]`

วงเล็บที่ว่างเปล่าจะรวมกันตามรหัสผลิตภัณฑ์ภายในการแบ่งพาร์ติชัน

การจัดทำดัชนีจะกำหนดวิธีการที่คุณสามารถจัดกลุ่มผลลัพธ์ของคุณตามการตั้งค่าการสอบถาม `groupBy` ในกรณีนี้ ถ้าคุณไม่ได้กำหนดค่า `groupBy` ใดๆ คุณจะได้รับผลรวมตาม `productid` มิฉะนั้น ถ้าคุณกำหนด `groupBy` เป็น `groupBy=ColorId&groupBy=SizeId` คุณจะได้รับบรรทัดหลายบรรทัดที่ส่งคืน โดยยึดตามชุดสีและขนาดต่างๆ ในระบบ

คุณสามารถกำหนดเกณฑ์การสอบถามของคุณในเนื้อหาของคำขอ

ต่อไปนี้เป็นการสอบถามตัวอย่างเกี่ยวกับผลิตภัณฑ์ที่มีชุดสีและขนาด

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>การวัดแบบกำหนดเอง

ปริมาณการประเมินเริ่มต้นจะเชื่อมโยงกับ Supply Chain Management อย่างไรก็ตาม คุณอาจต้องการมีปริมาณที่รวมกันของชุดการประเมินเริ่มต้น เมื่อต้องการดำเนินการนี้ คุณสามารถมีการตั้งค่าคอนฟิกของปริมาณที่กำหนดเอง ซึ่งจะถูกเพิ่มเข้าไปในผลลัพธ์ของการสอบถามปริมาณคงคลังคงเหลือ

ฟังก์ชันนี้จะช่วยให้คุณสามารถกำหนดชุดของการวัดที่จะเพิ่ม และ/หรือชุดของการวัดที่จะถูกลบ เพื่อสร้างการวัดที่กำหนดเอง

ตัวอย่างเช่น ด้วยเงื่อนไขการสอบถามต่อไปนี้ คุณจะตั้งค่าคอนฟิกปริมาณการวัดแบบกำหนดเองเป็น `MyCustomAvailableforReservation` ที่จะใช้โดยระบบปริมาณการใช้วัสดุ

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| ระบบปริมาณการใช้วัสดุ | ผู้วัดที่มีการคำนวณ | แหล่งข้อมูล | ตัวแก้ไข | ชนิดการคำนวณของตัวแก้ไข |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | การเพิ่มขึ้น |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | การเพิ่มขึ้น |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | การลบ |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | การเพิ่มขึ้น |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | การลบ |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | การเพิ่มขึ้น |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | การเพิ่มขึ้น |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | การลบ |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | การลบ |

การสอบถามในปริมาณการวัดที่กำหนดเองจะส่งคืนผลลัพธ์ต่อไปนี้

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

ผลลัพธ์ `MyCustomAvailableforReservation` จะขึ้นอยู่กับการตั้งค่าการคำนวณในการวัดที่กำหนดเองเป็น:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ

URL ที่แน่นอนซึ่งจะมีการโพสต์เหตุการณ์ จะขึ้นอยู่กับภูมิภาคทางภูมิศาสตร์ของคุณ ซึ่งจะใช้ฟอร์ม:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

เมื่อมีการพิสูจน์ตัวจริง สามารถใช้ URL นี้พร้อมกับวิธีการ HTTP `POST` เพื่อส่งเหตุการณ์ของการเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปยังบริการ

ส่วนหัวพิเศษจะถูกใช้สำหรับการสื่อสารกับบริการ Dynamics 365 ผ่านคำขอ HTTP ซึ่งแสดงรหัสสภาพแวดล้อมของอินสแตนซ์ Supply Chain Management ที่ข้อมูลถูกลิงค์ไปถึง ตัวอย่างเช่น:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 1

ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณจะตั้งค่าการตั้งค่าคอนฟิกมิติใน Power Apps

ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 2

ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` เป็น null ว่างเปล่า หรือช่องว่าง

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>คุณสมบัติฟิลด์ของเอกสาร JSON

ฟิลด์จากตัวอย่างการสอบถาม JSON ที่ให้ไว้ก่อนหน้านี้ มีคุณสมบัติที่แสดงรายการอยู่ในตารางต่อไปนี้

| ฟิลด์ ID | คำอธิบาย |
|---|---|
| `id` | รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ รหัสนี้จะใช้เพื่อให้แน่ใจว่า ถ้าการสื่อสารกับบริการล้มเหลวในระหว่างการโพสต์ การส่งเหตุการณ์อีกครั้งจะไม่มีผลในเหตุการณ์เดียวกันที่ถูกนับสองครั้งในระบบ |
| `organizationId` | ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์ นี่จะแม็ปไปยังองค์กร Supply Chain Management หรือรหัสพื้นที่ข้อมูล |
| `productId` | ตัวระบุของผลิตภัณฑ์ที่สงสัย |
| `quantity` | ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ ตัวอย่างเช่น ถ้าตัวอย่างเช่น เบเกิลใหม่ 10 ชิ้นถูกเพิ่มไปยังชั้นวาง ค่านี้จะเป็น 10 ถ้าเบเกิล 3 ชิ้นถูกเอาออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น -3 |
| `dimensionDataSource` | แหล่งข้อมูลของมิติที่ใช้ในการโพสต์เหตุการณ์การเปลี่ยนแปลงและการสอบถาม ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้ ด้วยการตั้งค่าคอนฟิกมิติ ความสามารถในการมองเห็นสินค้าคงคลังสามารถแม็ปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป ถ้าไม่มีการระบุ `dimensionDataSource` คุณสามารถใช้มิติเริ่มต้นทั่วไปในการสอบถามของคุณเท่านั้น   |
| `dimensions` | ถุงแบบไดนามิกของคู่คีย์/ค่า การทำเช่นนี้จะแม็ปกับบางมิติใน Supply Chain Management แต่คุณยังสามารถเพิ่มมิติที่กำหนดเองได้ด้วย (เช่น *แหล่งที่มา*) ซึ่งอาจแสดงว่าเหตุการณ์นี้มาจาก Supply Chain Management หรือระบบภายนอก |

### <a name="querying-current-on-hand"></a>การสอบถามปริมาณคงคลังคงเหลือปัจจุบัน

ปลายทางสำหรับการสอบถามปริมาณคงคลังคงเหลือปัจจุบันจะมี URL ที่คล้ายกัน:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

ซึ่งจะมีการสอบถามด้วยวิธีการ HTTP `POST`

#### <a name="current-on-hand-query-example-1"></a>ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 1

ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณดำเนินการการตั้งค่าคอนฟิกมิติเสร็จสมบูรณ์แล้วใน Power Apps

ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ คุณสามารถระบุ `DimensionDataSource` ใน `filters` และระบุมิติที่กำหนดเองในทั้ง `filters` และ `groupByValues` ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 2

ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` ภายใต้ `filters` เป็น null ว่างเปล่า หรือช่องว่าง

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>ผลลัพธ์การส่งคืนตัวอย่าง

การสอบถามที่แสดงในตัวอย่างก่อนหน้านี้ อาจส่งผลให้เกิดผลลัพธ์ดังนี้

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

โปรดสังเกตว่าฟิลด์ปริมาณมีการจัดโครงสร้างเป็นพจนานุกรมของการวัดและค่าที่เกี่ยวข้อง


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
