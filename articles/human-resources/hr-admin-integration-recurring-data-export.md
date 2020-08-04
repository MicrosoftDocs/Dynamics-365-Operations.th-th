---
title: สร้างแอปการส่งออกข้อมูลที่เกิดซ้ำ
description: บทความนี้แสดงวิธีการสร้างแอปตรรกะ Microsoft Azure ที่ส่งออกข้อมูลจาก Microsoft Dynamics 365 Human Resources บนกำหนดการที่เกิดซ้ำ
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010688"
---
# <a name="create-a-recurring-data-export-app"></a>สร้างแอปการส่งออกข้อมูลที่เกิดซ้ำ

บทความนี้แสดงวิธีการสร้างแอปตรรกะ Microsoft Azure ที่ส่งออกข้อมูลจาก Microsoft Dynamics 365 Human Resources บนกำหนดการที่เกิดซ้ำ บทสอนใช้ประโยชน์จากอินเทอร์เฟสโปรแกรมแอปพลิเคชัน (API) REST แพคเกจ DMF ของฝ่ายทรัพยากรบุคคลเพื่อส่งออกข้อมูล หลังจากที่มีการส่งออกข้อมูล แอปตรรกะจะบันทึกแพคเกจข้อมูลที่ส่งออกไปยัง Microsoft OneDrive สำหรับโฟลเดอร์ธุรกิจ

## <a name="business-scenario"></a>สถานการณ์จำลองทางธุรกิจ

ในสถานการณ์จำลองธุรกิจโดยทั่วไปหนึ่ง ๆ สำหรับการรวม Microsoft Dynamics 365 ต้องส่งออกข้อมูลไปยังระบบแบบดาวน์สตรีมบนกำหนดการที่เกิดซ้ำ บทสอนแสดงวิธีการส่งออกเรกคอร์ดผู้ปฏิบัติงานทั้งหมดจาก Microsoft Dynamics 365 Human Resources และบันทึกรายการของผู้ปฏิบัติงานใน OneDrive สำหรับโฟลเดอร์ธุรกิจ

> [!TIP]
> ข้อมูลเฉพาะที่ส่งออกในบทสอนนี้และปลายทางของข้อมูลที่ส่งออกเป็นตัวอย่างเท่านั้น คุณสามารถเปลี่ยนเพื่อให้ตรงกับความต้องการของธุรกิจของคุณได้อย่างง่ายดาย

## <a name="technologies-used"></a>เทคโนโลยีที่ใช้

บทสอนนี้ใช้เทคโนโลยีต่อไปนี้:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – แหล่งข้อมูลหลักสำหรับผู้ปฏิบัติงานที่จะส่งออก
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – เทคโนโลยีที่ให้การประสานกันและการจัดกำหนดการของการส่งออกที่เกิดซ้ำ

    - **[ตัวเชื่อมต่อ](https://docs.microsoft.com/azure/connectors/apis-list)** – เทคโนโลยีที่ใช้ในการเชื่อมต่อแอปตรรกะกับปลายทางที่ต้องการ

        - [HTTP กับตัวเชื่อมต่อ Azure AD](https://docs.microsoft.com/connectors/webcontents/)
        - [OneDrive สำหรับตัวเชื่อมต่อธุรกิจ](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)

- **[API REST แพคเกจ DMF](../dev-itpro/data-entities/data-management-api.md)** – เทคโนโลยีที่ใช้เพื่อทริกเกอร์การส่งออกและตรวจสอบความคืบหน้า
- **[OneDrive สำหรับธุรกิจ](https://onedrive.live.com/about/business/)** – ปลายทางสำหรับผู้ปฏิบัติงานที่ส่งออก

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้นการออกกำลังกายในบทสอนนี้ คุณต้องมีสินค้าต่อไปนี้:

- สภาพแวดล้อมของฝ่ายทรัพยากรบุคคลที่มีสิทธิ์ระดับผู้ดูแลระบบในสภาพแวดล้อม
- [การบอกรับเป็นสมาชิก Azure](https://azure.microsoft.com/free/) เพื่อโฮสต์แอปตรรกะ

## <a name="the-exercise"></a>แบบฝึกหัด

เมื่อสิ้นสุดแบบฝึกหัดนี้ คุณจะมีแอปตรรกะที่เชื่อมต่อกับสภาพแวดล้อมของทรัพยากรบุคคลและ OneDrive สำหรับบัญชีธุรกิจของคุณ แอปตรรกะจะส่งออกแพคเกจข้อมูลจากทรัพยากรบุคคล รอให้การส่งออกเสร็จสมบูรณ์ ดาวน์โหลดแพคเกจข้อมูลที่ส่งออก และบันทึกแพ็คเกจข้อมูลใน OneDrive สำหรับโฟลเดอร์ธุรกิจที่คุณระบุ

แอปตรรกะที่เสร็จสมบูรณ์จะมีลักษณะภาพประกอบต่อไปนี้

![ภาพรวมของแอปตรรกะ](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>ขั้นตอนที่ 1: สร้างโครงการส่งออกข้อมูลในทรัพยากรบุคคล

ในทรัพยากรบุคคล สร้างโครงการส่งออกข้อมูลที่ส่งออกผู้ปฏิบัติงาน ตั้งชื่อโครงการ **ส่งออกผู้ปฏิบัติงาน** และตรวจสอบให้แน่ใจว่าตัวเลือก **สร้างแพคเกจข้อมูล** ถูกตั้งค่าเป็น **ใช่** เพิ่มหนึ่งเอนทิตีเดียวของ (**ผู้ปฏิบัติงาน**) ให้กับโครงการและเลือกรูปแบบที่จะส่งออก (รูปแบบ Microsoft Excel ที่ใช้ในบทสอนนี้)

![ส่งออกโครงการข้อมูลผู้ปฏิบัติงาน](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> จำชื่อของโครงการส่งออกข้อมูล คุณจะต้องใช้เมื่อคุณสร้างแอปตรรกะในขั้นตอนต่อไป

### <a name="step-2-create-the-logic-app"></a>ขั้นตอนที่ 2: สร้างแอปตรรกะ

แบบฝึกหัดจำนวนมากเกี่ยวข้องกับการสร้างแอปตรรกะ

1. ในพอร์ทัล Azure ให้สร้างแอปตรรกะ

    ![หน้าการสร้างแอปตรรกะ](media/integration-logic-app-creation-1.png)

2. ใน Logic Apps Designer เริ่มต้นด้วยแอปตรรกะเปล่า
3. เพิ่ม [ทริกเกอร์การจัดการการเกิดซ้ำ](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) เพื่อรันแอปตรรกะทุก 24 ชั่วโมง (หรือตามกำหนดการที่คุณเลือก)

    ![กล่องโต้ตอบการเกิดซ้ำ](media/integration-logic-app-recurrence-step.png)

4. เรียก DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) เพื่อกำหนดตารางเวลาการส่งออกของแพคเกจข้อมูลของคุณ

    1. ใช้การดำเนินการ **เรียกคำขอ** HTTP ที่มีตัวเชื่อมต่อ Azure AD

        - **URL ของทรัพยากรพื้นฐาน:** URL ของสภาพแวดล้อมของทรัพยากรบุคคล (ไม่รวมข้อมูลพาธ/namespace)
        - **URI ทรัพยากร Azure AD:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > บริการของฝ่ายทรัพยากรบุคคลยังไม่ได้ให้ตัวเชื่อมต่อที่แสดง API ทั้งหมดที่สร้าง API REST ของแพคเกจ DMF เช่น **ExportToPackage** แทนที่จะทำเช่นนั้น คุณต้องเรียก API โดยใช้การร้องขอข้อมูลดิบของ HTTPS ผ่าน HTTP โดยใช้ตัวเชื่อมต่อ Azure AD ตัวเชื่อมต่อนี้ใช้ Azure Active Directory (Azure AD) สำหรับการรับรองความถูกต้องและการตรวจสอบความถูกต้องของทรัพยากรบุคคล

        ![HTTP กับตัวเชื่อมต่อ Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. ลงชื่อเข้าสู่สภาพแวดล้อมของทรัพยากรบุคคลด้วย HTTP ที่มีตัวเชื่อมต่อ Azure AD
    3. ตั้งค่าคำร้องขอ HTTP **POST** เพื่อเรียก DMF REST API **ExportToPackage**

        - **วิธีการ:** POST
        - **Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **เนื้อหาของคำขอ**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![เรียกการดำเนินการคำขอ HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > คุณอาจต้องการเปลี่ยนชื่อแต่ละขั้นตอนเพื่อให้มีความสำคัญมากกว่าชื่อเริ่มต้น **เรียกใช้คำขอ HTTP** ตัวอย่างเช่น คุณสามารถเปลี่ยนชื่อขั้นตอนนี้ **ExportToPackage**

5. [เริ่มต้นตัวแปร](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) เพื่อจัดเก็บสถานะการดำเนินการของคำขอ **ExportToPackage**

    ![เริ่มต้นการดำเนินการผันแปร](media/integration-logic-app-initialize-variable-step.png)

6. รอจนกว่าสถานะการดำเนินการของการส่งออกข้อมูลเป็น **เสร็จเรียบร้อยแล้ว**

    1. เพิ่มการ [วนรอบ](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) ที่มีการทำซ้ำจนกว่าค่าของตัวแปร **ExecutionStatus** เป็น **เสร็จเรียบร้อยแล้ว**
    2. เพิ่มการดำเนินการ **ล่าช้า** ที่รอห้าวินาทีก่อนที่จะทำการสำรวจสำหรับสถานะการดำเนินการปัจจุบันของการส่งออก

        ![จนถึงคอนเทนเนอร์ลูป](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > ตั้งค่าจำนวนจำกัดที่ **15** เพื่อให้รอเวลาสูงสุด 75 วินาที (15 การเกิดซ้ำ × 5 วินาที) ให้การส่งออกเสร็จสมบูรณ์ ถ้าการส่งออกของคุณใช้เวลานานขึ้น ให้ปรับจำนวนขีดจำกัดตามความเหมาะสม        

    3. เพิ่มการดำเนินการ **เรียกคำขอ HTTP** DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) และตั้งค่าตัวแปร **ExecutionStatus** เป็นผลลัพธ์ของการตอบสนอง **GetExecutionSummaryStatus**

        > ตัวอย่างนี้ไม่ทำการตรวจสอบข้อผิดพลาด API **GetExecutionSummaryStatus** สามารถส่งคืนสถานะเทอร์มินัลที่ไม่สำเร็จ (นั่นคือสถานะอื่นๆ ที่ไม่ใช่ **สำเร็จ**) สำหรับข้อมูลเพิ่มเติม ให้ดูที่[เอกสาร API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus)

        - **วิธีการ:** POST
        - **Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **เนื้อหาของคำขอ:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > คุณอาจต้องป้อนค่า **เนื้อหาของคำขอ** อย่างใดอย่างหนึ่งในมุมมองรหัสหรือในโปรแกรมแก้ไขฟังก์ชันในตัวออกแบบ

        ![เรียกการดำเนินการคำขอ HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![ตั้งค่าการดำเนินการผันแปร](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > ค่าสำหรับการดำเนิน **การตั้งค่าตัวแปร** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) จะแตกต่างจากค่าสำหรับค่าเนื้อหา **เรียกใช้คำร้องขอ HTTP 2** ถึงแม้ว่าตัวออกแบบจะแสดงค่าในลักษณะเดียวกัน

7. รับ URL การดาวน์โหลดแพคเกจที่ส่งออก

    - เพิ่มการดำเนินการ **เรียกใช้คำขอ HTTP** เพื่อเรียก DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl)

        - **วิธีการ:** POST
        - **Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **เนื้อหาของคำขอ:** {"executionId": body(' GetExportedPackageURL')?[value']}

        ![การดำเนินการ GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. ดาวน์โหลดข้อมูลแพคเกจที่ส่งออก

    - เพิ่มการร้องขอ HTTP **รับ** ([การดำเนินการของตัวเชื่อมต่อ HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http) ที่มีอยู่ในตัว) เพื่อดาวน์โหลดแพคเกจจาก URL ที่ส่งคืนในขั้นตอนก่อนหน้านี้

        - **วิธีการ:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > คุณอาจต้องป้อนค่า **URI** อย่างใดอย่างหนึ่งในมุมมองรหัสหรือในโปรแกรมแก้ไขฟังก์ชันในตัวออกแบบ

        ![การดำเนินการรับ HTTP](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > คำขอนี้ไม่จำเป็นต้องมีการตรวจสอบความถูกต้อง เนื่องจาก URL ที่ API **GetExportedPackageUrl** ส่งคืน มีโทเคนลายเซ็นการเข้าถึงที่ใช้ร่วมกันที่ให้สิทธิ์เข้าถึงเพื่อดาวน์โหลดไฟล์

9. บันทึกแพคเกจที่ดาวน์โหลดโดยใช้ตัวเชื่อมต่อ [OneDrive สำหรับธุรกิจ](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)

    - เพิ่มการดำเนินการ OneDrive สำหรับธุกิจ [สร้างไฟล์](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file)
    - เชื่อมต่อกับ OneDrive ของคุณกับบัญชีธุรกิจตามต้องการ

        - **พาธของโฟลเดอร์:** โฟลเดอร์ที่คุณเลือก
        - **ชื่อไฟล์:** worker\_package.zip
        - **เนื้อหาของไฟล์:** เนื้อหาจากขั้นตอนก่อนหน้านี้ (เนื้อหาแบบไดนามิก)

        ![การสร้างไฟล์การดำเนินการ](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>ขั้นตอนที่ 3: ทดสอบแอปตรรกะ

เมื่อต้องการทดสอบแอปตรรกะ เลือกปุ่ม **รัน** ในตัวออกแบบ คุณจะเห็นว่าขั้นตอนของแอปตรรกะเริ่มต้นที่จะรัน หลังจากวินาทีที่ 30 จนถึง 40 ควรรันแอปตรรกะจนเสร็จสิ้น และ OneDrive สำหรับโฟลเดอร์ธุรกิจของคุณควรรวมไฟล์แพคเกจใหม่ที่มีผู้ปฏิบัติงานที่ส่งออก

ถ้ามีการรายงานความล้มเหลวสำหรับขั้นตอนใดๆ ให้เลือกขั้นตอนที่ล้มเหลวตัวออกแบบ และตรวจสอบฟิลด์ **ข้อมูลป้อนเข้า** และ **เอาต์พุต** ตรวจแก้จุดบกพร่องและปรับเปลี่ยนขั้นตอนตามต้องการเพื่อแก้ไขข้อผิดพลาด

ภาพประกอบต่อไปนี้แสดงลักษณะการทำงานของ Logic Apps Designer เมื่อขั้นตอนทั้งหมดของแอปตรรกะรันเสร็จเรียบร้อยแล้ว

![การรันแอปตรรกะสำเร็จ](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>สรุป

ในบทสอนนี้ คุณเรียนรู้วิธีใช้แอปตรรกะเพื่อส่งออกข้อมูลจากทรัพยากรบุคคลและบันทึกข้อมูลที่ส่งออกไปยัง OneDrive สำหรับโฟลเดอร์ธุรกิจ คุณสามารถแก้ไขขั้นตอนของบทสอนนี้ได้ตามความจำเป็นเพื่อให้เหมาะสมกับความต้องการของธุรกิจของคุณ


