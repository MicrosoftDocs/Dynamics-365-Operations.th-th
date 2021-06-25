---
title: การตั้งค่าคอนฟิกสำหรับ Finance Insights สำหรับตัวอย่างสาธารณะ (ตัวอย่าง) - รุ่น 10.0.20 และรุ่นที่ใหม่กว่า
description: หัวข้อนี้จะอธิบายการตั้งค่าคอนฟิกระบบของคุณเพื่อใช้ความสามารถที่มีอยู่ใน Finance insights สำหรับตัวอย่างสาธารณะในรุ่น 10.0.20 และรุ่นที่ใหม่กว่า
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222623"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="5756b-103">การตั้งค่าคอนฟิกสำหรับ Finance Insights สำหรับตัวอย่างสาธารณะ (ตัวอย่าง) - รุ่น 10.0.20 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5756b-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5756b-104">ข้อมูลเชิงลึก Finance รวมฟังก์ชันจาก Microsoft Dynamics 365 Finance พร้อมกับ Dataverse, Azure และ AI Builder เพื่อให้เครื่องมือการคาดการณ์ที่มีประสิทธิภาพสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="5756b-105">หัวข้อนี้จะอธิบายการตั้งค่าคอนฟิก Dynamics 365 Finance รุ่น 10.0.20 เพื่อให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ใน Finance insights สำหรับตัวอย่างสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="5756b-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="5756b-106">ขั้นตอนการตั้งค่าคอนฟิกที่อธิบายไว้ในหัวข้อนี้จะใช้เฉพาะกับ Finance รุ่น 10.0.20 และรุ่นที่ใหม่กว่าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5756b-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="5756b-107">หากต้องการตั้งค่า Finance Insights รุ่น 10.0.19 และเก่ากว่า ให้ดูที่ [การตั้งค่าคอนฟิกของ Finance insights - รุ่นสูงสุด 10.0.18](configure-for-fin-insites.md)</span><span class="sxs-lookup"><span data-stu-id="5756b-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="5756b-108">ปรับใช้ Finance</span><span class="sxs-lookup"><span data-stu-id="5756b-108">Deploy Finance</span></span>

<span data-ttu-id="5756b-109">ให้ทำตามขั้นตอนเหล่านี้เพื่อปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5756b-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="5756b-110">ใน Microsoft Dynamics Lifecycle Services (LCS) สร้างหรืออัปเดตข้อมูลสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="5756b-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="5756b-111">สภาพแวดล้อมต้องมีแอปรุ่น 10.0.20 หรือ Finance and Operations ที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="5756b-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="5756b-112">สภาพแวดล้อมต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูง (HA) ใน Sandbox</span><span class="sxs-lookup"><span data-stu-id="5756b-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="5756b-113">(สภาพแวดล้อมชนิดนี้เรียกอีกอย่างว่า สภาพแวดล้อมระดับ 2) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="5756b-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="5756b-114">ถ้าคุณกําหนดค่าการเงินให้กับ Finance Insights ในสภาพแวดล้อม Sandbox คุณอาจต้องคัดลอกข้อมูลการผลิตไปยังสภาพแวดล้อมนั้นเพื่อให้การคาดการณ์สามารถทำงานได้</span><span class="sxs-lookup"><span data-stu-id="5756b-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="5756b-115">แบบจำลองการคาดการณ์จะใช้ข้อมูลหลายปีเพื่อสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="5756b-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="5756b-116">ข้อมูลสาธิต Contoso มีข้อมูลในอดีตไม่เพียงพอที่จะการฝึกอบรมแบบจำลองอย่างเพียงพอ</span><span class="sxs-lookup"><span data-stu-id="5756b-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="5756b-117">ตั้งค่าคอนฟิก Dataverse</span><span class="sxs-lookup"><span data-stu-id="5756b-117">Configure Dataverse</span></span>

<span data-ttu-id="5756b-118">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าคอนฟิก Dataverse สำหรับ Finance Insights</span><span class="sxs-lookup"><span data-stu-id="5756b-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="5756b-119">ใน LCS เปิดหน้าสภาพแวดล้อมและตรวจสอบว่าส่วน **การรวม Power Platform** ได้รับการตั้งค่าเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="5756b-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="5756b-120">ถ้ามีการตั้งค่าไว้แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="5756b-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="5756b-121">ถ้าไม่มีการตั้งค่า ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="5756b-122">ในส่วน **การรวม Power Platform** เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="5756b-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="5756b-123">การตั้งค่าสภาพแวดล้อมอาจใช้เวลาถึงหนึ่งชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="5756b-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="5756b-124">ถ้ามีการตั้งค่าสภาพแวดล้อม Dataverse ไว้เสร็จสมบูรณ์แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Finance</span><span class="sxs-lookup"><span data-stu-id="5756b-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5756b-125">เมื่อคุณเสร็จสิ้นการตั้งค่าสภาพแวดล้อมแล้ว **อย่า** เลือก **ลิงค์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="5756b-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="5756b-126">ปุ่มนี้ไม่เป็นปุ่มที่ไม่ต้องการสำหรับ Finance Insights</span><span class="sxs-lookup"><span data-stu-id="5756b-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="5756b-127">หากคุณเลือก Add-in ของสภาพแวดล้อมที่กําหนดใน LCS คุณจะไม่สามารถตั้งค่าคอนฟิก Add-in ของสภาพแวดล้อมที่กําหนดได้</span><span class="sxs-lookup"><span data-stu-id="5756b-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="5756b-128">ตั้งค่าคอนฟิก Azure</span><span class="sxs-lookup"><span data-stu-id="5756b-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="5756b-129">ใช้ Azure Cloud Shell เพื่อตั้งค่าทรัพยากร Data Lake ของข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="5756b-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="5756b-130">ใช้สคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5756b-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="5756b-131">มีการให้สคริปต์ Windows PowerShell ไว้ เพื่อให้คุณสามารถตั้งค่าทรัพยากร Azure ที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการส่งออกไปยัง Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="5756b-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="5756b-132">ถ้าคุณต้องการดำเนินการตั้งค่าด้วยตนเอง ให้ข้ามกระบวนงานนี้ และดำเนินการต่อด้วยกระบวนงานในส่วน [การตั้งค่าด้วยตนเอง](#manual-setup) แทน</span><span class="sxs-lookup"><span data-stu-id="5756b-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="5756b-133">ใช้ขั้นตอนต่อไปนี้เพื่อรันสคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5756b-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="5756b-134">การตั้งค่าอาจใช้ไม่ได้ หากคุณใช้ตัวเลือก **ทดลองใช้** ใน Azure CLI หรือหากคุณรันสคริปต์บนคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="5756b-135">ทำตามขั้นตอนต่อไปนี้โดยใช้สคริปต์ Windows PowerShell เพื่อตั้งค่าคอนฟิก Azure</span><span class="sxs-lookup"><span data-stu-id="5756b-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="5756b-136">คุณต้องมีสิทธิ์ในการสร้างกลุ่มทรัพยากร Azure ทรัพยากร Azure และแอปพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="5756b-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="5756b-137">สำหรับข้อมูลเกี่ยวกับสิทธิ์ที่จำเป็น ให้ดูที่ [ตรวจสอบสิทธิ์ Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)</span><span class="sxs-lookup"><span data-stu-id="5756b-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="5756b-138">ใน [พอร์ทัล azure](https://portal.azure.com) ให้ไปที่การบอกรับเป็นสมาชิก Azure เป้าหมายของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="5756b-139">เลือก **Cloud Shell** ทางด้านขวาของฟิลด์ **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="5756b-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="5756b-140">เลือก **PowerShell**</span><span class="sxs-lookup"><span data-stu-id="5756b-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="5756b-141">สร้างที่เก็บข้อมูล ถ้าคุณได้รับพร้อมท์ให้สร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="5756b-142">บนแท็บ **Azure CLI** เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="5756b-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="5756b-143">ใน Notepad ให้เปิดไฟล์ใหม่และวางในสคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5756b-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="5756b-144">บันทึกไฟล์เป็น **ConfigureDataLake.ps1**</span><span class="sxs-lookup"><span data-stu-id="5756b-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="5756b-145">อัพโหลดสคริปต์ Windows PowerShell ไปยังรอบเวลาโดยใช้ตัวเลือกเมนูเพื่ออัพโหลดใน Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="5756b-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="5756b-146">รันสคริปต์ **.\ConfigureDataLake.ps1**</span><span class="sxs-lookup"><span data-stu-id="5756b-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="5756b-147">ติดตามพร้อมท์เพื่อรันสคริปต์</span><span class="sxs-lookup"><span data-stu-id="5756b-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="5756b-148">ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อติดตั้ง add-in ส่งออกไปยัง Data Lake ใน LCS</span><span class="sxs-lookup"><span data-stu-id="5756b-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="5756b-149">การตั้งค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5756b-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="5756b-150">เพิ่มแอปพลิเคชันในผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="5756b-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="5756b-151">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="5756b-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="5756b-152">เลือก **จัดการ \> แอปพลิเคชันองค์กร**</span><span class="sxs-lookup"><span data-stu-id="5756b-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="5756b-153">ค้นหาแอปพลิเคชันต่อไปนี้ตามรหัสของแอป</span><span class="sxs-lookup"><span data-stu-id="5756b-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="5756b-154">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="5756b-154">Application</span></span>                              | <span data-ttu-id="5756b-155">รหัสแอพ</span><span class="sxs-lookup"><span data-stu-id="5756b-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="5756b-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="5756b-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="5756b-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="5756b-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="5756b-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="5756b-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="5756b-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="5756b-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="5756b-160">บริการตรวจสอบ AI Builder</span><span class="sxs-lookup"><span data-stu-id="5756b-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="5756b-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="5756b-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="5756b-162">ถ้าคุณไม่พบแอปพลิเคชันก่อนหน้าใดๆ ให้ลองทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5756b-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="5756b-163">บนคอมพิวเตอร์เฉพาะที่ของคุณ ให้เลือกเมนู **เริ่มต้น** ค้นหา **powershell**</span><span class="sxs-lookup"><span data-stu-id="5756b-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="5756b-164">เลือกและกดค้างไว้ (หรือคลิกขวา) **Windows PowerShell** และจากนั้น เลือก **เรียกใช้ในฐานะผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="5756b-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="5756b-165">รันคำสั่งต่อไปนี้เพื่อติดตั้งโมดูล **AzureAD**</span><span class="sxs-lookup"><span data-stu-id="5756b-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="5756b-166">ถ้าต้องการให้ผู้ให้บริการ NuGet ดำเนินการต่อ ให้เลือก **Y** เพื่อติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="5756b-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="5756b-167">ถ้าคุณได้รับข้อความ "ที่เก็บที่ไม่น่าเชื่อถือ" ให้เลือก **Y** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="5756b-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="5756b-168">สำหรับแต่ละแอปพลิเคชันที่ต้องมีการเพิ่ม ให้รันคำสั่งต่อไปนี้เพื่อเพิ่มแอปพลิเคชันไปยัง Azure AD</span><span class="sxs-lookup"><span data-stu-id="5756b-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="5756b-169">เมื่อคุณได้รับพร้อมท์ ให้ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบ Azure AD</span><span class="sxs-lookup"><span data-stu-id="5756b-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="5756b-170">สร้างแหล่งข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="5756b-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="5756b-171">ตรวจสอบให้แน่ใจว่าคุณได้สร้างทรัพยากรต่อไปนี้ในอินสแตนซ์ Azure AD ที่เหมือนกันกับสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="5756b-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="5756b-172">คุณไม่สามารถใช้ทรัพยากรจากอินสแตนซ์ Azure AD อื่นได้</span><span class="sxs-lookup"><span data-stu-id="5756b-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="5756b-173">การสร้างบัญชีที่จัดเก็บ:</span><span class="sxs-lookup"><span data-stu-id="5756b-173">Create a storage account:</span></span>

    1. <span data-ttu-id="5756b-174">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้างบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="5756b-175">ในกล่องโต้ตอบ **สร้างบัญชีที่จัดเก็บ** ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="5756b-176">**สถานที่** – เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="5756b-177">**ประสิทธิภาพ** – เราขอแนะนำให้คุณเลือก **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="5756b-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="5756b-178">**ชนิดบัญชี** – คุณต้องเลือก **StorageV2**</span><span class="sxs-lookup"><span data-stu-id="5756b-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="5756b-179">ในกล่องโต้ตอบ **ตัวเลือกขั้นสูง** สำหรับตัวเลือก **Data Lake storage Gen2** เลือก **เปิดใช้งาน** ภายใต้คุณลักษณะ **namespaces ตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="5756b-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="5756b-180">ถ้าคุณไม่เปิดใช้งานคุณลักษณะนี้ คุณไม่สามารถใช้ข้อมูลที่แอป Finance and Operations เขียนโดยใช้บริการต่างๆ เช่น โฟลว์ข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="5756b-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="5756b-181">เลือก **รีวิวและสร้าง**</span><span class="sxs-lookup"><span data-stu-id="5756b-181">Select **Review and create**.</span></span> <span data-ttu-id="5756b-182">เมื่อการปรับใช้งานเสร็จสมบูรณ์ จะมีการแสดงทรัพยากรใหม่ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="5756b-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="5756b-183">ไปที่บัญชีจัดเก็บข้อมูลที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="5756b-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="5756b-184">บนเมนูด้านซ้าย ให้เลือก **คีย์การเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="5756b-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="5756b-185">คัดลอกและบันทึกชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="5756b-186">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault</span><span class="sxs-lookup"><span data-stu-id="5756b-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="5756b-187">สร้าง Key Vault:</span><span class="sxs-lookup"><span data-stu-id="5756b-187">Create a key vault:</span></span>

    1. <span data-ttu-id="5756b-188">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้าง Key Vault</span><span class="sxs-lookup"><span data-stu-id="5756b-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="5756b-189">ในกล่องโต้ตอบ **สร้าง Key Vault** ในฟิลด์ **สถานที่** ให้เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="5756b-190">หลังจากที่สร้าง key vault แล้ว ให้ไปที่ **ภาพรวม Key Vault** และคัดลอกและบันทึกชื่อ DNS</span><span class="sxs-lookup"><span data-stu-id="5756b-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="5756b-191">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่า add-in ของ Data Lake</span><span class="sxs-lookup"><span data-stu-id="5756b-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="5756b-192">สร้างและลงทะเบียนแอปพลิเคชัน Azure AD:</span><span class="sxs-lookup"><span data-stu-id="5756b-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="5756b-193">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory** แล้วจากนั้น เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="5756b-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="5756b-194">เลือก **การลงทะเบียนแอปพลิเคชันใหม่** และตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="5756b-195">**ชื่อ** – ป้อนชื่อของแอป</span><span class="sxs-lookup"><span data-stu-id="5756b-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="5756b-196">**ชนิดของแอปพลิเคชัน** – เลือก **Web API**</span><span class="sxs-lookup"><span data-stu-id="5756b-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="5756b-197">**เปลี่ยนเส้นทางการตั้งค่า URI** – ป้อน URL สำหรับอินสแตนซ์ Dynamics 365 ของคุณ เช่น `https://yourdynamicsinstance.dynamics.com/auth`</span><span class="sxs-lookup"><span data-stu-id="5756b-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="5756b-198">ไปที่แอปพลิเคชันที่คุณเพิ่งสร้างขึ้น และคัดลอกและบันทึกค่า **รหัสของแอปพลิเคชัน (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="5756b-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="5756b-199">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault</span><span class="sxs-lookup"><span data-stu-id="5756b-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="5756b-200">ไปที่ **สิทธิ์ของ API** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="5756b-201">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="5756b-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="5756b-202">เลือก **Azure Key Vault**</span><span class="sxs-lookup"><span data-stu-id="5756b-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="5756b-203">หลังจากที่คุณเลือกสิทธิ์ที่ได้รับมอบหมาย ให้เลือก **ผู้ใช้\_การเลียนแบบ**</span><span class="sxs-lookup"><span data-stu-id="5756b-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="5756b-204">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="5756b-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="5756b-205">บนเมนูสำหรับแอป ให้เลือก **ใบรับรอง \& ข้อมูลลับ** และจากนั้น ทำตามขั้นตอนต่อไปนี้เพื่อสร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="5756b-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="5756b-206">เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5756b-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="5756b-207">ในฟิลด์ **คำอธิบาย Key** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="5756b-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="5756b-208">เลือกระยะเวลา แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5756b-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="5756b-209">ข้อมูลลับจะถูกสร้างขึ้นในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="5756b-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="5756b-210">คัดลอกและบันทึกค่าข้อมูลลับไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="5756b-210">Copy and save the client secret value.</span></span> <span data-ttu-id="5756b-211">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่าข้อมูลลับ key vault</span><span class="sxs-lookup"><span data-stu-id="5756b-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="5756b-212">สร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="5756b-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="5756b-213">ไปที่ Key Vault ที่คุณสร้างไว้ก่อนหน้านี้ และเลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="5756b-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="5756b-214">สำหรับชื่อลับแต่ละชื่อในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="5756b-215">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="5756b-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="5756b-216">ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="5756b-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="5756b-217">สร้างชื่อและค่าลับจากตาราง</span><span class="sxs-lookup"><span data-stu-id="5756b-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="5756b-218">เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5756b-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="5756b-219">ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="5756b-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="5756b-220">ชื่อข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="5756b-220">Secret name</span></span>                       | <span data-ttu-id="5756b-221">ค่าลับ</span><span class="sxs-lookup"><span data-stu-id="5756b-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="5756b-222">รหัสแอป</span><span class="sxs-lookup"><span data-stu-id="5756b-222">app-id</span></span>                            | <span data-ttu-id="5756b-223">รหัสแอปของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5756b-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="5756b-224">ข้อมูลลับของแอป</span><span class="sxs-lookup"><span data-stu-id="5756b-224">app-secret</span></span>                        | <span data-ttu-id="5756b-225">ข้อมูลลับของไคลเอนต์ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5756b-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="5756b-226">ชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-226">storage-account-name</span></span>              | <span data-ttu-id="5756b-227">ชื่อของบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้ เช่น **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="5756b-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="5756b-228">อนุญาตให้แอปพลิเคชันเข้าถึง key vault:</span><span class="sxs-lookup"><span data-stu-id="5756b-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="5756b-229">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิด key vault ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5756b-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="5756b-230">เลือกนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5756b-230">Select the access policies.</span></span>
    3. <span data-ttu-id="5756b-231">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="5756b-232">เลือก **เพิ่มนโยบายการเข้าถึง** เพื่อสร้างนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="5756b-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="5756b-233">ในฟิลด์ **สิทธิ์ของข้อมูลลับ** ให้เลือกสิทธิ์จากตาราง</span><span class="sxs-lookup"><span data-stu-id="5756b-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="5756b-234">ในฟิลด์ **หลักการเลือก** ให้ค้นหาชื่อที่แสดงของแอปพลิเคชันจากตาราง</span><span class="sxs-lookup"><span data-stu-id="5756b-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="5756b-235">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="5756b-235">Select **Select**.</span></span>
        5. <span data-ttu-id="5756b-236">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="5756b-236">Select **Add**.</span></span>
        6. <span data-ttu-id="5756b-237">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5756b-237">Select **Save**.</span></span>

        | <span data-ttu-id="5756b-238">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="5756b-238">Application</span></span>                                              | <span data-ttu-id="5756b-239">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="5756b-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="5756b-240">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-240">The display name of the new application that you created</span></span> | <span data-ttu-id="5756b-241">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="5756b-241">Get, List</span></span>   |
        | <span data-ttu-id="5756b-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="5756b-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="5756b-243">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="5756b-243">Get, List</span></span>   |

6. <span data-ttu-id="5756b-244">กำหนดบทบาทที่จะเข้าถึงบัญชีที่จัดเก็บ:</span><span class="sxs-lookup"><span data-stu-id="5756b-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="5756b-245">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิดบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="5756b-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="5756b-246">เลือก **การควบคุมการเข้าถึง (IAM)** และจากนั้น เลือก **การกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="5756b-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="5756b-247">เลือก **เพิ่ม เพิ่มการกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="5756b-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="5756b-248">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="5756b-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="5756b-249">เลือกบทบาทจากตาราง</span><span class="sxs-lookup"><span data-stu-id="5756b-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="5756b-250">ปล่อยฟิลด์ **กำหนดการเข้าถึงแก่** ให้มีการตั้งค่าเป็น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**</span><span class="sxs-lookup"><span data-stu-id="5756b-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="5756b-251">ในฟิลด์ **เลือก** ให้ป้อนแอปพลิเคชันจากตาราง</span><span class="sxs-lookup"><span data-stu-id="5756b-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="5756b-252">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5756b-252">Select **Save**.</span></span>

        | <span data-ttu-id="5756b-253">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="5756b-253">Application</span></span>                                              | <span data-ttu-id="5756b-254">บทบาท</span><span class="sxs-lookup"><span data-stu-id="5756b-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="5756b-255">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-255">The display name of the new application that you created</span></span> | <span data-ttu-id="5756b-256">เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="5756b-256">Owner</span></span>                       |
        | <span data-ttu-id="5756b-257">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-257">The display name of the new application that you created</span></span> | <span data-ttu-id="5756b-258">ผู้จ่ายสมทบ</span><span class="sxs-lookup"><span data-stu-id="5756b-258">Contributor</span></span>                 |
        | <span data-ttu-id="5756b-259">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-259">The display name of the new application that you created</span></span> | <span data-ttu-id="5756b-260">ผู้สนับสนุนบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="5756b-261">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="5756b-261">The display name of the new application that you created</span></span> | <span data-ttu-id="5756b-262">เจ้าของข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="5756b-263">**บริการตรวจสอบ AI Builder**</span><span class="sxs-lookup"><span data-stu-id="5756b-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="5756b-264">ตัวอ่านข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="5756b-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5756b-265">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="5756b-266">ตั้งค่าคอนฟิกการส่งออกไปยัง add-in ของ Data Lake</span><span class="sxs-lookup"><span data-stu-id="5756b-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="5756b-267">ทำตามขั้นตอนต่อไปนี้เพื่อใช้ LCS เพื่อเพิ่มการส่งออกไปยัง add-in ของ Data Lake ไปยังสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5756b-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="5756b-268">ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5756b-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="5756b-269">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5756b-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="5756b-270">เลือก add-in **ส่งออกไปยัง Data Lake**</span><span class="sxs-lookup"><span data-stu-id="5756b-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="5756b-271">ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5756b-271">Enter the following values.</span></span>

    | <span data-ttu-id="5756b-272">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="5756b-272">Value</span></span>                                                              | <span data-ttu-id="5756b-273">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5756b-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="5756b-274">รหัสผู้เช่าของการบอกรับเป็นสมาชิก Azure ที่เป็นที่ตั้งของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="5756b-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="5756b-275">รหัสผู้เช่าซึ่งเป็นที่ตั้งของบัญชีที่จัดเก็บ แอป และ Key Vault</span><span class="sxs-lookup"><span data-stu-id="5756b-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="5756b-276">หากต้องการได้รับค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="5756b-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="5756b-277">ระบุชื่อ DNS ของ Key Vault ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5756b-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="5756b-278">ชื่อ DNS ของ Key Vault เช่น `https://customkeyvault.vault.azure.net/`</span><span class="sxs-lookup"><span data-stu-id="5756b-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="5756b-279">ระบุข้อมูลลับที่มีชื่อของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="5756b-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="5756b-280">**ชื่อ-บัญชี-ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="5756b-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="5756b-281">ชื่อลับสำหรับรหัสแอปที่จะใช้สำหรับการเข้าถึง Data Lake</span><span class="sxs-lookup"><span data-stu-id="5756b-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="5756b-282">**รหัส-แอป**</span><span class="sxs-lookup"><span data-stu-id="5756b-282">**app-id**</span></span> |
    | <span data-ttu-id="5756b-283">ชื่อข้อมูลลับของข้อมูลลับไคลเอนต์แอป</span><span class="sxs-lookup"><span data-stu-id="5756b-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="5756b-284">**ข้อมูลลับ-แอป**</span><span class="sxs-lookup"><span data-stu-id="5756b-284">**app-secret**</span></span> |

5. <span data-ttu-id="5756b-285">ยอมรับเงื่อนไข และเลือกจากนั้น **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="5756b-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="5756b-286">จะมีการติดตั้ง add-in ภายในสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="5756b-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="5756b-287">ตั้งค่าคอนฟิก add-in ของ Finance Insights</span><span class="sxs-lookup"><span data-stu-id="5756b-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="5756b-288">ถ้าคุณติดตั้ง Add-in ของรับข้อมูลเชิงลึกไว้ก่อนหน้านี้ ให้ถอนการติดตั้งก่อนที่คุณจะสามารถปฏิบัติตามขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="5756b-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="5756b-289">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อติดตั้ง Add-in ของ Finance Insights</span><span class="sxs-lookup"><span data-stu-id="5756b-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="5756b-290">ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="5756b-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="5756b-291">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5756b-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="5756b-292">เลือก add-in ของ **Finance Insights**</span><span class="sxs-lookup"><span data-stu-id="5756b-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="5756b-293">ยอมรับเงื่อนไข และเลือกจากนั้น **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="5756b-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="5756b-294">ผลป้อนกลับและการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="5756b-294">Feedback and support</span></span>

<span data-ttu-id="5756b-295">หากคุณมีความสนใจในการให้ผลป้อนกลับ หรือหากคุณต้องการความช่วยเหลือ โปรดส่งอีเมล์ถึง [Finance insights (ตัวอย่าง)](mailto:fiap@microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="5756b-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
