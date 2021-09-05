---
title: ตั้งค่าการแสดงผลสินค้าคงคลัง
description: หัวข้อนี้จะอธิบายวิธีการติดตั้ง Add-in การแสดงผลสินค้าคงคลังสำหรับ Microsoft Dynamics 365 Supply Chain Management
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343595"
---
# <a name="set-up-inventory-visibility"></a>ตั้งค่าการแสดงผลสินค้าคงคลัง

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

หัวข้อนี้จะอธิบายวิธีการติดตั้ง Add-in การแสดงผลสินค้าคงคลังสำหรับ Microsoft Dynamics 365 Supply Chain Management

คุณจำเป็นต้องใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อติดตั้ง Add-in การแสดงผลสินค้าคงคลัง LCS เป็นพอร์ทัลการทำงานร่วมกันที่ให้สภาพแวดล้อมและชุดของบริการที่อัปเดตเป็นประจำ ซึ่งช่วยให้คุณสามารถจัดการวงจรการใช้งานแอปพลิเคชันของแอป Finance and Operations ของคุณได้

สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)

## <a name="inventory-visibility-prerequisites"></a>ข้อกำหนดเบื้องต้นของการแสดงผลสินค้าคงคลัง

ก่อนที่คุณจะสามารถติดตั้งการแสดงผลสินค้าคงคลัง คุณต้องดำเนินการงานต่อไปนี้ให้เสร็จ:

- รับโครงการสำหรับการใช้งาน LCS โดยมีสภาพแวดล้อมที่ปรับใช้อย่างน้อยหนึ่งรายการ
- ตรวจสอบให้แน่ใจว่าข้อกำหนดเบื้องต้นของการตั้งค่า Add-in เสร็จสมบูรณ์แล้ว สำหรับข้อมูลเพิ่มเติมเกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ ให้ดูที่ [ภาพรวม Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) Inventory Visibility ไม่ต้องการการเชื่อมโยงแบบสองทิศทาง
- ติดต่อทีมงานผลิตภัณฑ์การแสดงผลสินค้าคงคลังที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์ที่ต้องการไฟล์ต่อไปนี้:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (ถ้าเวอร์ชันของ Supply Chain Management ที่คุณรันอยู่เป็นรุ่นก่อนหน้าเวอร์ชัน 10.0.18)

> [!NOTE]
> ปัจจุบันประเทศและภูมิภาคที่ได้รับการสนับสนุนได้แก่ แคนาดา (URI, ECA) สหรัฐอเมริกา (USDS, EUS) สหภาพยุโรป (USD, WEU) สหราชอาณาจักร (USD, USD) และออสเตรเลีย (URI, WEU)

ถ้าคุณมีคำถามใดๆ เกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ ติดต่อทีมงานผลิตภัณฑ์ของการแสดงผลสินค้าคงคลัง

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>ตั้งค่า Dataverse

หากต้องการตั้งค่า Dataverse เพื่อให้สามารถใช้กับการแสดงผลสินค้าคงคลังใช้เครื่องมือ Package Deployer เพื่อปรับใช้แพคเกจการแสดงผลสินค้าคงคลัง ส่วนย่อยต่อไปนี้อธิบายถึงวิธีทำงานแต่ละรายการให้เสร็จ

> [!NOTE]
> ปัจจุบัน สนับสนุนเฉพาะสภาพแวดล้อม Dataverse ที่สร้างโดยใช้ LCS เท่านั้น ถ้าสภาพแวดล้อม Dataverse ของคุณถูกสร้างขึ้นในวิธีอื่น (ตัวอย่างเช่น โดยใช้ศูนย์การจัดการ Power Apps) และถ้าจะเชื่อมโยงกับสภาพแวดล้อม Supply Chain Management ของคุณ คุณต้องติดต่อทีมงานผลิตภัณฑ์การแสดงผลสินค้าคงคลังเพื่อแก้ปัญหาการแม็ปก่อน จากนั้นคุณสามารถติดตั้งการแสดงผลสินค้าคงคลัง

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>ย้ายจากรุ่นเก่าของโซลูชัน Dataverse

หากคุณติดตั้งโซลูชัน Dataverse ของการแสดงผลสินค้าคงคลังรุ่นกว่า ให้ใช้คําแนะนําเหล่านี้เพื่ออัปเดตรุ่นของคุณ มีสองกรณีดังต่อไปนี้

- **กรณีที่ 1:** หากคุณตั้งค่า Dataverse ด้วยตนเองโดยการนําเข้าโซลูชัน `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` ให้ปฏิบัติตามขั้นตอนต่อไปนี้

    1. ดาวน์โหลดสามไฟล์ต่อไปนี้

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. นําเข้า `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` และ `InventoryServiceBase_managed.cab` เข้าไปที่ Dataverse ด้วยตนเองตามขั้นตอนต่อไปนี้

        1. เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ
        1. เปิดหน้า **โซลูชัน**
        1. เลือก **นำเข้า**

    1. ใช้เครื่องมือ Package Deployer เพื่อจัดวางแพคเกจ `InventoryServiceApplication.PackageDeployer.zip` สำหรับคำแนะนำ ให้ดูที่ส่วน [ใช้เครื่องมือ Package Deployer เพื่อจัดวางแพคเกจ](#deploy-package) ในหัวข้อนี้ในภายหลัง

- **กรณีที่ 2:** ถ้าคุณตั้งค่า Dataverse โดยใช้เครื่องมือ Package Deployer ก่อนที่คุณจะติดตั้งแพคเกจ `.*PackageDeployer.zip` เก่า ดาวน์โหลด `InventoryServiceApplication.PackageDeployer.zip` และอัปเดต สำหรับคำแนะนำ ให้ดูที่ส่วน [ใช้เครื่องมือ Package Deployer เพื่อจัดวางแพคเกจ](#deploy-package)

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>ใช้เครื่องมือ Package Deployer เพื่อจัดวางแพคเกจ

1. ติดตั้งเครื่องมือของนักพัฒนาตามที่อธิบายไว้ใน [ดาวน์โหลดจาก NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget)
1. ยกเลิกการบล็อคไฟล์ `InventoryServiceApplication.PackageDeployer.zip` ที่คุณดาวน์โหลดจากกลุ่ม Teams โดยปฏิบัติตามขั้นตอนต่อไปนี้

    1. เลือกค้างไว้ (หรือคลิกขวา) ที่ไฟล์ แล้วเลือก **คุณสมบัติ**
    1. ในกล่องโต้ตอบ **คุณสมบัติ** บนแท็บ **ทั่วไป** ให้ค้นหาส่วน **ความปลอดภัย** เลือก **ยกเลิกการบล็อค** และใช้การเปลี่ยนแปลง ถ้าไม่มีส่วน **ความปลอดภัย** บนแท็บ **ทั่วไป** ไฟล์จะไม่ถูกบล็อค ในกรณีนี้ ให้ดำเนินการต่อไปยังขั้นตอนถัดไป

    ![ยกเลิกการบล็อคไฟล์ที่ดาวน์โหลด](media/unblock-file.png "ยกเลิกการบล็อคไฟล์ที่ดาวน์โหลด")

1. แตกไฟล์ `InventoryServiceApplication.PackageDeployer.zip` เพื่อค้นหารายการต่อไปนี้:

    - โฟลเดอร์ `InventoryServiceApplication`
    - ไฟล์ `[Content_Types].xml`
    - ไฟล์ `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`

1. คัดลอกแต่ละรายการไปยังไดเรกทอรี `.\Tools\PackageDeployment` (ไดเรกทอรีนี้สร้างขึ้นเมื่อคุณติดตั้งเครื่องมือของนักพัฒนา)
1. เรียกใช้ `.\Tools\PackageDeployment\PackageDeployer.exe` และปฏิบัติตามคําแนะนําบนหน้าจอเพื่อนําเข้าโซลูชัน

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง

ก่อนที่คุณจะติดตั้ง Add-in ให้ลงทะเบียนโปรแกรมประยุกต์และเพิ่มข้อมูลลับไคลเอนต์ลงใน Azure Active Directory (Azure AD) ภายใต้การบอกรับเป็นสมาชิก Azure ของคุณ สำหรับคำแนะนำ ให้ดูที่ [ลงทะเบียนโปรแกรมประยุกต์](/azure/active-directory/develop/quickstart-register-app) และ [เพิ่มข้อมูลลับไคลเอนต์](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) ตรวจสอบให้แน่ใจว่าได้จดบันทึก **รหัสโปรแกรมประยุกต์ (ไคลเอนต์)** **ข้อมูลลับไคลเอนต์** และ **รหัสผู้เช่า** เนื่องจากคุณจะต้องใช้ในภายหลัง

หลังจากที่คุณลงทะเบียนโปรแกรมประยุกต์และเพิ่มข้อมูลลับไคลเอนต์ไปยัง Azure AD แล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อติดตั้ง Add-in ของการแสดงผลสินค้าคงคลัง

1. ลงชื่อเข้าใช้ [LCS](https://lcs.dynamics.com/Logon/Index)
1. บนโฮมเพจ ให้เลือกโครงการที่มีการปรับใช้สภาพแวดล้อมของคุณ
1. บนหน้าโครงการ ให้เลือกสภาพแวดล้อมที่คุณต้องการติดตั้ง add-in
1. ในหน้าสภาพแวดล้อม ให้เลื่อนลงจนกว่าคุณจะพบส่วน **Add-in ของสภาพแวดล้อม** ในส่วน **การรวม Power Platform** คุณสามารถค้นหาชื่อสภาพแวดล้อม Dataverse ได้
1. ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**

    ![หน้าสภาพแวดล้อมใน LCS](media/inventory-visibility-environment.png "หน้าสภาพแวดล้อมใน LCS")

1. เลือกลิงก์ **ติดตั้ง Add-in ใหม่** รายการของ add-in ที่พร้อมใช้งานจะเปิดขึ้น
1. ในรายการ เลือก **การแสดงผลสินค้าคงคลัง**
1. ให้กำหนดฟิลด์ดังต่อไปนี้สำหรับสภาพแวดล้อมของคุณ:

    - **รหัสโปรแกรมประยุกต์ AAD (ไคลเอนต์)** – ป้อนรหัสโปรแกรมประยุกต์ Azure AD ที่คุณสร้างไว้และจดบันทึกก่อนหน้านี้
    - **รหัสผู้เช่า AAD** – ป้อนรหัสผู้เช่าที่คุณจดบันทึกไว้ก่อนหน้านี้

    ![ตั้งค่าหน้า Add in](media/inventory-visibility-setup.png "ตั้งค่าหน้า Add in")

1. ยอมรับข้อกำหนดและเงื่อนไขโดยเลือกกล่องกาเครื่องหมาย **ข้อกำหนดและเงื่อนไข**
1. เลือก **ติดตั้ง** สถานะของ add-in จะแสดงเป็น **กำลังติดตั้ง** เมื่อการติดตั้งเสร็จสมบูรณ์ รีเฟรชหน้า สถานะควรเปลี่ยนแปลงเป็น **ติดตั้งแล้ว**

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>ถอนการติดตั้ง Add-in การแสดงผลสินค้าคงคลัง

เมื่อต้องการถอนการติดตั้ง Add-in ของการแสดงผลสินค้าคงคลัง ให้เลือก **ถอนการติดตั้ง** ในหน้า LCS กระบวนการถอนการติดตั้งจะยุติ Add-in การแสดงผลสินค้าคงคลัง ยกเลิกการลงทะเบียน Add-in จาก LCS และลบข้อมูลชั่วคราวใดๆ ที่จัดเก็บไว้ในแคชข้อมูล Add-in การแสดงผลสินค้าคงคลัง อย่างไรก็ตาม ข้อมูลสินค้าคงคลังหลักที่จัดเก็บไว้ในการสมัครใช้งาน Dataverse ของคุณจะไม่ถูกลบ

เมื่อต้องการถอนการติดตั้งข้อมูลสินค้าคงคลังที่ถูกจัดเก็บไว้ในการสมัครใช้งาน Dataverse ของคุณ ให้เปิด [Power Apps](https://make.powerapps.com) เลือก **สภาพแวดล้อม** บนแถบนําทาง และเลือกสภาพแวดล้อม Dataverse ที่มีความสัมพันธ์กับสภาพแวดล้อม LCS ของคุณ จากนั้นไปที่ **โซลูชัน** และลบโซลูชันห้าวิธีต่อไปนี้

- โซลูชันจุดยึดของโปรแกรมประยุกต์การแสดงผลสินค้าคงคลังในโซลูชัน Dynamics 365
- โซลูชันโปรแกรมประยุกต์การแสดงผลสินค้าคงคลังของ Dynamics 365 FNO SCM
- การตั้งค่าคอนฟิกบริการสินค้าคงคลัง
- การแสดงผลสินค้าคงคลังแบบสแตนด์อโลน
- โซลูชันพื้นฐานของการแสดงผลสินค้าคงคลังของ Dynamics 365 FNO SCM

หลังจากที่คุณลบโซลูชันเหล่านี้แล้ว ข้อมูลที่จัดเก็บอยู่ในตารางจะถูกลบด้วย

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>ตั้งค่า Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>ปรับใช้แพคเกจการรวมการแสดงผลสินค้าคงคลัง

ถ้าคุณรัน Supply Chain Management เวอร์ชัน 10.0.17 หรือก่อนหน้านั้น ให้ติดต่อทีมสนับสนุนการแสดงผลสินค้าคงคลัง ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์แพคเกจ แล้วปรับใช้แพคเกจใน LCS

> [!NOTE]
> ถ้าเกิดข้อผิดพลาดที่ไม่ตรงกันของเวอร์ชันระหว่างการปรับใช้ คุณต้องนําเข้าโครงการ X++ ด้วยตนเอง ลงในสภาพแวดล้อมการพัฒนาของคุณ จากนั้นสร้างแพคเกจที่สามารถปรับใช้งานได้ในสภาพแวดล้อมการพัฒนาของคุณ และปรับใช้ในสภาพแวดล้อมการทำงานจริงของคุณ
>
> รหัสถูกรวมอยู่กับ Supply Chain Management เวอร์ชัน 10.0.18 ถ้าคุณรันเวอร์ชันนั้นอยู่หรือเวอร์ชันที่ใหม่กว่า ไม่ต้องมีการปรับใช้

ตรวจสอบให้แน่ใจว่าคุณลักษณะต่อไปนี้ได้เปิดใช้งานอยู่ในสภาพแวดล้อม Supply Chain Management ของคุณ (โดยค่าเริ่มต้น จะเปิดใช้งาน)

| คำอธิบายลักษณะการทำงาน | เวอร์ชันรหัส | สลับคลาส |
|---|---|---|
| เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง

1. ใน Supply Chain Management ให้เปิดพื้นที่ทำงาน **[การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** และเปิดคุณลักษณะ *การรวมการแสดงผลสินค้าคงคลัง*
1. ไปที่ **การจัดการสินค้าคงคลัง \> ตั้งค่า \> พารามิเตอร์การรวมการแสดงผลสินค้าคงคลัง** และป้อน URL ของสภาพแวดล้อมที่คุณรันการแสดงผลสินค้าคงคลังอยู่ สำหรับข้อมูลเพิ่มเติม ดู [ค้นหาปลายทางบริการ](inventory-visibility-power-platform.md#get-service-endpoint)
1. ไปที่ **การจัดการสินค้าคงคลัง \> ประจำงวด \> การรวมการแสดงผลสินค้าคงคลัง** และเปิดใช้งานงาน ขณะนี้เหตุการณ์การเปลี่ยนแปลงสินค้าคงคลังทั้งหมดจาก Supply Chain Management จะถูกลงรายการบัญชีไปยังการแสดงผลสินค้าคงคลัง

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
