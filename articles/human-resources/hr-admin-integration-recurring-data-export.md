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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420804"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="4133a-103">สร้างแอปการส่งออกข้อมูลที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4133a-103">Create a recurring data export app</span></span>

<span data-ttu-id="4133a-104">บทความนี้แสดงวิธีการสร้างแอปตรรกะ Microsoft Azure ที่ส่งออกข้อมูลจาก Microsoft Dynamics 365 Human Resources บนกำหนดการที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4133a-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="4133a-105">บทสอนใช้ประโยชน์จากอินเทอร์เฟสโปรแกรมแอปพลิเคชัน (API) REST แพคเกจ DMF ของฝ่ายทรัพยากรบุคคลเพื่อส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4133a-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="4133a-106">หลังจากที่มีการส่งออกข้อมูล แอปตรรกะจะบันทึกแพคเกจข้อมูลที่ส่งออกไปยัง Microsoft OneDrive สำหรับโฟลเดอร์ธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4133a-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="4133a-107">สถานการณ์จำลองทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4133a-107">Business scenario</span></span>

<span data-ttu-id="4133a-108">ในสถานการณ์จำลองธุรกิจโดยทั่วไปหนึ่ง ๆ สำหรับการรวม Microsoft Dynamics 365 ต้องส่งออกข้อมูลไปยังระบบแบบดาวน์สตรีมบนกำหนดการที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4133a-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="4133a-109">บทสอนแสดงวิธีการส่งออกเรกคอร์ดผู้ปฏิบัติงานทั้งหมดจาก Microsoft Dynamics 365 Human Resources และบันทึกรายการของผู้ปฏิบัติงานใน OneDrive สำหรับโฟลเดอร์ธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4133a-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="4133a-110">ข้อมูลเฉพาะที่ส่งออกในบทสอนนี้และปลายทางของข้อมูลที่ส่งออกเป็นตัวอย่างเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4133a-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="4133a-111">คุณสามารถเปลี่ยนเพื่อให้ตรงกับความต้องการของธุรกิจของคุณได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="4133a-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="4133a-112">เทคโนโลยีที่ใช้</span><span class="sxs-lookup"><span data-stu-id="4133a-112">Technologies used</span></span>

<span data-ttu-id="4133a-113">บทสอนนี้ใช้เทคโนโลยีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4133a-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="4133a-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – แหล่งข้อมูลหลักสำหรับผู้ปฏิบัติงานที่จะส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="4133a-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – เทคโนโลยีที่ให้การประสานกันและการจัดกำหนดการของการส่งออกที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4133a-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="4133a-116">**[ตัวเชื่อมต่อ](https://docs.microsoft.com/azure/connectors/apis-list)** – เทคโนโลยีที่ใช้ในการเชื่อมต่อแอปตรรกะกับปลายทางที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4133a-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="4133a-117">[HTTP กับตัวเชื่อมต่อ Azure AD](https://docs.microsoft.com/connectors/webcontents/)</span><span class="sxs-lookup"><span data-stu-id="4133a-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="4133a-118">[OneDrive สำหรับตัวเชื่อมต่อธุรกิจ](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="4133a-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="4133a-119">**[API REST แพคเกจ DMF](../dev-itpro/data-entities/data-management-api.md)** – เทคโนโลยีที่ใช้เพื่อทริกเกอร์การส่งออกและตรวจสอบความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="4133a-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="4133a-120">**[OneDrive สำหรับธุรกิจ](https://onedrive.live.com/about/business/)** – ปลายทางสำหรับผู้ปฏิบัติงานที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4133a-121">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4133a-121">Prerequisites</span></span>

<span data-ttu-id="4133a-122">ก่อนที่คุณจะเริ่มต้นการออกกำลังกายในบทสอนนี้ คุณต้องมีสินค้าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4133a-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="4133a-123">สภาพแวดล้อมของฝ่ายทรัพยากรบุคคลที่มีสิทธิ์ระดับผู้ดูแลระบบในสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="4133a-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="4133a-124">[การบอกรับเป็นสมาชิก Azure](https://azure.microsoft.com/free/) เพื่อโฮสต์แอปตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4133a-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="4133a-125">แบบฝึกหัด</span><span class="sxs-lookup"><span data-stu-id="4133a-125">The exercise</span></span>

<span data-ttu-id="4133a-126">เมื่อสิ้นสุดแบบฝึกหัดนี้ คุณจะมีแอปตรรกะที่เชื่อมต่อกับสภาพแวดล้อมของทรัพยากรบุคคลและ OneDrive สำหรับบัญชีธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="4133a-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="4133a-127">แอปตรรกะจะส่งออกแพคเกจข้อมูลจากทรัพยากรบุคคล รอให้การส่งออกเสร็จสมบูรณ์ ดาวน์โหลดแพคเกจข้อมูลที่ส่งออก และบันทึกแพ็คเกจข้อมูลใน OneDrive สำหรับโฟลเดอร์ธุรกิจที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="4133a-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="4133a-128">แอปตรรกะที่เสร็จสมบูรณ์จะมีลักษณะภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4133a-128">The completed logic app will resemble the following illustration.</span></span>

![ภาพรวมของแอปตรรกะ](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="4133a-130">ขั้นตอนที่ 1: สร้างโครงการส่งออกข้อมูลในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4133a-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="4133a-131">ในทรัพยากรบุคคล สร้างโครงการส่งออกข้อมูลที่ส่งออกผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="4133a-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="4133a-132">ตั้งชื่อโครงการ **ส่งออกผู้ปฏิบัติงาน** และตรวจสอบให้แน่ใจว่าตัวเลือก **สร้างแพคเกจข้อมูล** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4133a-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="4133a-133">เพิ่มหนึ่งเอนทิตีเดียวของ (**ผู้ปฏิบัติงาน**) ให้กับโครงการและเลือกรูปแบบที่จะส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="4133a-134">(รูปแบบ Microsoft Excel ที่ใช้ในบทสอนนี้)</span><span class="sxs-lookup"><span data-stu-id="4133a-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![ส่งออกโครงการข้อมูลผู้ปฏิบัติงาน](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="4133a-136">จำชื่อของโครงการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4133a-136">Remember the name of the data export project.</span></span> <span data-ttu-id="4133a-137">คุณจะต้องใช้เมื่อคุณสร้างแอปตรรกะในขั้นตอนต่อไป</span><span class="sxs-lookup"><span data-stu-id="4133a-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="4133a-138">ขั้นตอนที่ 2: สร้างแอปตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4133a-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="4133a-139">แบบฝึกหัดจำนวนมากเกี่ยวข้องกับการสร้างแอปตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4133a-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="4133a-140">ในพอร์ทัล Azure ให้สร้างแอปตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4133a-140">In the Azure portal, create a logic app.</span></span>

    ![หน้าการสร้างแอปตรรกะ](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="4133a-142">ใน Logic Apps Designer เริ่มต้นด้วยแอปตรรกะเปล่า</span><span class="sxs-lookup"><span data-stu-id="4133a-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="4133a-143">เพิ่ม [ทริกเกอร์การจัดการการเกิดซ้ำ](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) เพื่อรันแอปตรรกะทุก 24 ชั่วโมง (หรือตามกำหนดการที่คุณเลือก)</span><span class="sxs-lookup"><span data-stu-id="4133a-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![กล่องโต้ตอบการเกิดซ้ำ](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="4133a-145">เรียก DMF REST API [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) เพื่อกำหนดตารางเวลาการส่งออกของแพคเกจข้อมูลของคุณ</span><span class="sxs-lookup"><span data-stu-id="4133a-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="4133a-146">ใช้การดำเนินการ **เรียกคำขอ** HTTP ที่มีตัวเชื่อมต่อ Azure AD</span><span class="sxs-lookup"><span data-stu-id="4133a-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="4133a-147">**URL ของทรัพยากรพื้นฐาน:** URL ของสภาพแวดล้อมของทรัพยากรบุคคล (ไม่รวมข้อมูลพาธ/namespace)</span><span class="sxs-lookup"><span data-stu-id="4133a-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="4133a-148">**URI ทรัพยากร Azure AD:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="4133a-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="4133a-149">บริการของฝ่ายทรัพยากรบุคคลยังไม่ได้ให้ตัวเชื่อมต่อที่แสดง API ทั้งหมดที่สร้าง API REST ของแพคเกจ DMF เช่น **ExportToPackage**</span><span class="sxs-lookup"><span data-stu-id="4133a-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="4133a-150">แทนที่จะทำเช่นนั้น คุณต้องเรียก API โดยใช้การร้องขอข้อมูลดิบของ HTTPS ผ่าน HTTP โดยใช้ตัวเชื่อมต่อ Azure AD</span><span class="sxs-lookup"><span data-stu-id="4133a-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="4133a-151">ตัวเชื่อมต่อนี้ใช้ Azure Active Directory (Azure AD) สำหรับการรับรองความถูกต้องและการตรวจสอบความถูกต้องของทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4133a-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP กับตัวเชื่อมต่อ Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="4133a-153">ลงชื่อเข้าสู่สภาพแวดล้อมของทรัพยากรบุคคลด้วย HTTP ที่มีตัวเชื่อมต่อ Azure AD</span><span class="sxs-lookup"><span data-stu-id="4133a-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="4133a-154">ตั้งค่าคำร้องขอ HTTP **POST** เพื่อเรียก DMF REST API **ExportToPackage**</span><span class="sxs-lookup"><span data-stu-id="4133a-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="4133a-155">**วิธีการ:** POST</span><span class="sxs-lookup"><span data-stu-id="4133a-155">**Method:** POST</span></span>
        - <span data-ttu-id="4133a-156">**Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="4133a-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="4133a-157">**เนื้อหาของคำขอ**</span><span class="sxs-lookup"><span data-stu-id="4133a-157">**Body of the request:**</span></span>

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
    > <span data-ttu-id="4133a-159">คุณอาจต้องการเปลี่ยนชื่อแต่ละขั้นตอนเพื่อให้มีความสำคัญมากกว่าชื่อเริ่มต้น **เรียกใช้คำขอ HTTP**</span><span class="sxs-lookup"><span data-stu-id="4133a-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="4133a-160">ตัวอย่างเช่น คุณสามารถเปลี่ยนชื่อขั้นตอนนี้ **ExportToPackage**</span><span class="sxs-lookup"><span data-stu-id="4133a-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="4133a-161">[เริ่มต้นตัวแปร](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) เพื่อจัดเก็บสถานะการดำเนินการของคำขอ **ExportToPackage**</span><span class="sxs-lookup"><span data-stu-id="4133a-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![เริ่มต้นการดำเนินการผันแปร](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="4133a-163">รอจนกว่าสถานะการดำเนินการของการส่งออกข้อมูลเป็น **เสร็จเรียบร้อยแล้ว**</span><span class="sxs-lookup"><span data-stu-id="4133a-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="4133a-164">เพิ่มการ [วนรอบ](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) ที่มีการทำซ้ำจนกว่าค่าของตัวแปร **ExecutionStatus** เป็น **เสร็จเรียบร้อยแล้ว**</span><span class="sxs-lookup"><span data-stu-id="4133a-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="4133a-165">เพิ่มการดำเนินการ **ล่าช้า** ที่รอห้าวินาทีก่อนที่จะทำการสำรวจสำหรับสถานะการดำเนินการปัจจุบันของการส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![จนถึงคอนเทนเนอร์ลูป](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="4133a-167">ตั้งค่าจำนวนจำกัดที่ **15** เพื่อให้รอเวลาสูงสุด 75 วินาที (15 การเกิดซ้ำ × 5 วินาที) ให้การส่งออกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="4133a-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="4133a-168">ถ้าการส่งออกของคุณใช้เวลานานขึ้น ให้ปรับจำนวนขีดจำกัดตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="4133a-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="4133a-169">เพิ่มการดำเนินการ **เรียกคำขอ HTTP** DMF REST API [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) และตั้งค่าตัวแปร **ExecutionStatus** เป็นผลลัพธ์ของการตอบสนอง **GetExecutionSummaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4133a-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="4133a-170">ตัวอย่างนี้ไม่ทำการตรวจสอบข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="4133a-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="4133a-171">API **GetExecutionSummaryStatus** สามารถส่งคืนสถานะเทอร์มินัลที่ไม่สำเร็จ (นั่นคือสถานะอื่นๆ ที่ไม่ใช่ **สำเร็จ**)</span><span class="sxs-lookup"><span data-stu-id="4133a-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="4133a-172">สำหรับข้อมูลเพิ่มเติม ให้ดูที่[เอกสาร API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus)</span><span class="sxs-lookup"><span data-stu-id="4133a-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="4133a-173">**วิธีการ:** POST</span><span class="sxs-lookup"><span data-stu-id="4133a-173">**Method:** POST</span></span>
        - <span data-ttu-id="4133a-174">**Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="4133a-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="4133a-175">**เนื้อหาของคำขอ:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="4133a-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="4133a-176">คุณอาจต้องป้อนค่า **เนื้อหาของคำขอ** อย่างใดอย่างหนึ่งในมุมมองรหัสหรือในโปรแกรมแก้ไขฟังก์ชันในตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="4133a-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![เรียกการดำเนินการคำขอ HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![ตั้งค่าการดำเนินการผันแปร](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="4133a-179">ค่าสำหรับการดำเนิน **การตั้งค่าตัวแปร** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) จะแตกต่างจากค่าสำหรับค่าเนื้อหา **เรียกใช้คำร้องขอ HTTP 2** ถึงแม้ว่าตัวออกแบบจะแสดงค่าในลักษณะเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4133a-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="4133a-180">รับ URL การดาวน์โหลดแพคเกจที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="4133a-181">เพิ่มการดำเนินการ **เรียกใช้คำขอ HTTP** เพื่อเรียก DMF REST API [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl)</span><span class="sxs-lookup"><span data-stu-id="4133a-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="4133a-182">**วิธีการ:** POST</span><span class="sxs-lookup"><span data-stu-id="4133a-182">**Method:** POST</span></span>
        - <span data-ttu-id="4133a-183">**Url ของคำขอ:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="4133a-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="4133a-184">**เนื้อหาของคำขอ:** {"executionId": body(' GetExportedPackageURL')?[value']}</span><span class="sxs-lookup"><span data-stu-id="4133a-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![การดำเนินการ GetExportedPackageURL](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="4133a-186">ดาวน์โหลดข้อมูลแพคเกจที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-186">Download the exported package.</span></span>

    - <span data-ttu-id="4133a-187">เพิ่มการร้องขอ HTTP **รับ** ([การดำเนินการของตัวเชื่อมต่อ HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http) ที่มีอยู่ในตัว) เพื่อดาวน์โหลดแพคเกจจาก URL ที่ส่งคืนในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4133a-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="4133a-188">**วิธีการ:** GET</span><span class="sxs-lookup"><span data-stu-id="4133a-188">**Method:** GET</span></span>
        - <span data-ttu-id="4133a-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="4133a-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="4133a-190">คุณอาจต้องป้อนค่า **URI** อย่างใดอย่างหนึ่งในมุมมองรหัสหรือในโปรแกรมแก้ไขฟังก์ชันในตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="4133a-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![การดำเนินการรับ HTTP](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="4133a-192">คำขอนี้ไม่จำเป็นต้องมีการตรวจสอบความถูกต้อง เนื่องจาก URL ที่ API **GetExportedPackageUrl** ส่งคืน มีโทเคนลายเซ็นการเข้าถึงที่ใช้ร่วมกันที่ให้สิทธิ์เข้าถึงเพื่อดาวน์โหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="4133a-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="4133a-193">บันทึกแพคเกจที่ดาวน์โหลดโดยใช้ตัวเชื่อมต่อ [OneDrive สำหรับธุรกิจ](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)</span><span class="sxs-lookup"><span data-stu-id="4133a-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="4133a-194">เพิ่มการดำเนินการ OneDrive สำหรับธุกิจ [สร้างไฟล์](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file)</span><span class="sxs-lookup"><span data-stu-id="4133a-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="4133a-195">เชื่อมต่อกับ OneDrive ของคุณกับบัญชีธุรกิจตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="4133a-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="4133a-196">**พาธของโฟลเดอร์:** โฟลเดอร์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="4133a-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="4133a-197">**ชื่อไฟล์:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="4133a-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="4133a-198">**เนื้อหาของไฟล์:** เนื้อหาจากขั้นตอนก่อนหน้านี้ (เนื้อหาแบบไดนามิก)</span><span class="sxs-lookup"><span data-stu-id="4133a-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![การสร้างไฟล์การดำเนินการ](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="4133a-200">ขั้นตอนที่ 3: ทดสอบแอปตรรกะ</span><span class="sxs-lookup"><span data-stu-id="4133a-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="4133a-201">เมื่อต้องการทดสอบแอปตรรกะ เลือกปุ่ม **รัน** ในตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="4133a-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="4133a-202">คุณจะเห็นว่าขั้นตอนของแอปตรรกะเริ่มต้นที่จะรัน</span><span class="sxs-lookup"><span data-stu-id="4133a-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="4133a-203">หลังจากวินาทีที่ 30 จนถึง 40 ควรรันแอปตรรกะจนเสร็จสิ้น และ OneDrive สำหรับโฟลเดอร์ธุรกิจของคุณควรรวมไฟล์แพคเกจใหม่ที่มีผู้ปฏิบัติงานที่ส่งออก</span><span class="sxs-lookup"><span data-stu-id="4133a-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="4133a-204">ถ้ามีการรายงานความล้มเหลวสำหรับขั้นตอนใดๆ ให้เลือกขั้นตอนที่ล้มเหลวตัวออกแบบ และตรวจสอบฟิลด์ **ข้อมูลป้อนเข้า** และ **เอาต์พุต**</span><span class="sxs-lookup"><span data-stu-id="4133a-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="4133a-205">ตรวจแก้จุดบกพร่องและปรับเปลี่ยนขั้นตอนตามต้องการเพื่อแก้ไขข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="4133a-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="4133a-206">ภาพประกอบต่อไปนี้แสดงลักษณะการทำงานของ Logic Apps Designer เมื่อขั้นตอนทั้งหมดของแอปตรรกะรันเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="4133a-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![การรันแอปตรรกะสำเร็จ](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="4133a-208">สรุป</span><span class="sxs-lookup"><span data-stu-id="4133a-208">Summary</span></span>

<span data-ttu-id="4133a-209">ในบทสอนนี้ คุณเรียนรู้วิธีใช้แอปตรรกะเพื่อส่งออกข้อมูลจากทรัพยากรบุคคลและบันทึกข้อมูลที่ส่งออกไปยัง OneDrive สำหรับโฟลเดอร์ธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4133a-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="4133a-210">คุณสามารถแก้ไขขั้นตอนของบทสอนนี้ได้ตามความจำเป็นเพื่อให้เหมาะสมกับความต้องการของธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="4133a-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


