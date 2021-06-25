---
title: การตั้งค่าคอนฟิกสำหรับ Finance Insights - ได้สูงสุดรุ่น 10.0.19
description: หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ใน Finance insights สูงสุดรุ่น 10.0.19
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186431"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="9cd97-103">การตั้งค่าคอนฟิกสำหรับข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="9cd97-104">ขั้นตอนต่อไปนี้สำหรับการตั้งค่า Finance Insights ใช้ได้กับ Microsoft Dynamics 365 Finance สูงสุดรุ่น 10.0.19</span><span class="sxs-lookup"><span data-stu-id="9cd97-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="9cd97-105">หากต้องการตั้งค่า Finance Insights รุ่น 10.0.20 และใหม่กว่า ให้ดูที่ [การตั้งค่าคอนฟิกของ Finance Insights (การแสดงตัวอย่าง) - รุ่น10.0.20 และอื่นๆ](configure-for-fin-insites-PubPrvw.md)</span><span class="sxs-lookup"><span data-stu-id="9cd97-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="9cd97-106">ข้อมูลเชิงลึก Finance รวมฟังก์ชันจาก Microsoft Dynamics 365 Finance พร้อมกับ Microsoft Dataverse, Azure และ AI Builder เพื่อให้เครื่องมือการคาดการณ์ที่มีประสิทธิภาพสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="9cd97-107">หัวข้อนี้จะอธิบายขั้นตอนการตั้งค่าคอนฟิกที่จะช่วยให้ระบบของคุณสามารถใช้ความสามารถที่มีอยู่ในข้อมูลเชิงลึก Finance ได้</span><span class="sxs-lookup"><span data-stu-id="9cd97-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="9cd97-108">ปรับใช้ Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="9cd97-109">ปรับใช้สภาพแวดล้อมโดยการทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="9cd97-110">ใน Microsoft Dynamics Lifecycle Services (LCS) สร้างหรืออัปเดตข้อมูลสภาพแวดล้อม Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="9cd97-111">สภาพแวดล้อมต้องมีแอปรุ่น 10.0.11/Platform update 35 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="9cd97-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="9cd97-112">สภาพแวดล้อมต้องมีสภาพแวดล้อมที่มีความพร้อมใช้งานสูง (HA) ใน Sandbox</span><span class="sxs-lookup"><span data-stu-id="9cd97-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="9cd97-113">(สภาพแวดล้อมชนิดนี้เรียกอีกอย่างว่า สภาพแวดล้อมระดับ 2) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)</span><span class="sxs-lookup"><span data-stu-id="9cd97-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="9cd97-114">ถ้าคุณกําหนดค่าการเงินให้กับ Finance Insights ในสภาพแวดล้อม Sandbox คุณอาจต้องคัดลอกข้อมูลการผลิตไปยังสภาพแวดล้อมนั้นเพื่อให้การคาดการณ์สามารถทำงานได้</span><span class="sxs-lookup"><span data-stu-id="9cd97-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="9cd97-115">แบบจำลองการคาดการณ์จะใช้ข้อมูลหลายปีเพื่อสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="9cd97-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="9cd97-116">ข้อมูลสาธิต Contoso มีข้อมูลในอดีตไม่เพียงพอที่จะการฝึกอบรมแบบจำลองอย่างเพียงพอ</span><span class="sxs-lookup"><span data-stu-id="9cd97-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="9cd97-117">ตั้งค่าคอนฟิก Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-117">Configure Dataverse</span></span>

<span data-ttu-id="9cd97-118">ใช้ขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิก Dataverse สำหรับ Finance Insights</span><span class="sxs-lookup"><span data-stu-id="9cd97-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="9cd97-119">เปิดหน้าสภาพแวดล้อมใน LCS และตรวจสอบว่าส่วน **การรวม Power Platform** ได้รับการตั้งค่าเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="9cd97-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="9cd97-120">ถ้ามีการตั้งค่าไว้แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="9cd97-121">คัดลอกชื่อสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="9cd97-122">ถ้าไม่มีการตั้งค่า ให้ทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="9cd97-123">เลือกปุ่ม **การตั้งค่า** ในส่วนการรวม Power Platform</span><span class="sxs-lookup"><span data-stu-id="9cd97-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="9cd97-124">ซึ่งอาจใช้เวลาถึงหนึ่งชั่วโมงเพื่อตั้งค่าสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9cd97-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="9cd97-125">ถ้ามีการตั้งค่าสภาพแวดล้อม Dataverse ไว้เสร็จสมบูรณ์แล้ว ควรแสดงรายการชื่อสภาพแวดล้อม Dataverse ที่เชื่อมโยงกับสภาพแวดล้อม Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="9cd97-126">คัดลอกชื่อสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="9cd97-127">หลังจากที่ตั้งค่าสภาพแวดล้อมเสร็จสมบูรณ์แล้ว **อย่า** เลือกปุ่ม **ลิงค์ไปยัง CDS for Apps**</span><span class="sxs-lookup"><span data-stu-id="9cd97-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="9cd97-128">นี่ไม่จำเป็นสำหรับ Finance Insights และจะปิดใช้งานความสามารถในการดำเนินการ Add-in ของสภาพแวดล้อมที่ต้องใช้ใน LCS ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9cd97-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="9cd97-129">เปิด [ศูนย์การจัดการ Power Platform](https://admin.powerplatform.microsoft.com/) และปฏิบัติตามขั้นตอนต่อไปนี้เพื่อสร้างสภาพแวดล้อม Dataverse ใหม่ในผู้เช่า Active Directory เดียวกัน:</span><span class="sxs-lookup"><span data-stu-id="9cd97-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="9cd97-130">เปิดหน้า **สภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="9cd97-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="9cd97-131">[![หน้าสภาพแวดล้อม](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="9cd97-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="9cd97-132">เลือกสภาพแวดล้อม Dataverse ที่สร้างไว้ด้านบน แล้วจากนั้น เลือก **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="9cd97-133">เลือก **ทรัพยากร \>การตั้งค่าดั้งเดิมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9cd97-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="9cd97-134">บนแถบนำทางบนสุด ให้เลือก **การตั้งค่า** แล้วจากนั้น เลือก **การเลือกกำหนด**</span><span class="sxs-lookup"><span data-stu-id="9cd97-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="9cd97-135">เลือก **ทรัพยากรของนักพัฒนา**</span><span class="sxs-lookup"><span data-stu-id="9cd97-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="9cd97-136">คัดลอกค่า **รหัสองค์กร Dataverse**</span><span class="sxs-lookup"><span data-stu-id="9cd97-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="9cd97-137">ในแถบที่อยู่ของเบราว์เซอร์ ให้จดบันทึก URL ขององค์กร Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="9cd97-138">ตัวอย่างเช่น URL อาจเป็น `https://org42b2b3d3.crm.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="9cd97-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="9cd97-139">ถ้าคุณวางแผนที่จะใช้คุณลักษณะการคาดการณ์กระแสเงินสดหรือคุณลักษณะการคาดการณ์งบประมาณ ให้ทำตามขั้นตอนต่อไปนี้เพื่ออัปเดตการจำกัดคำอธิบายสำหรับองค์กรของคุณเป็นอย่างน้อย 50 เมกะไบต์ (MB):</span><span class="sxs-lookup"><span data-stu-id="9cd97-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="9cd97-140">เปิด [พอร์ทัล Power Apps](https://make.powerapps.com)</span><span class="sxs-lookup"><span data-stu-id="9cd97-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="9cd97-141">เลือกสภาพแวดล้อมที่คุณเพิ่งสร้าง แล้วจากนั้น เลือก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="9cd97-142">เลือก **การตั้งค่า \> การตั้งค่าคอนฟิกอีเมล**</span><span class="sxs-lookup"><span data-stu-id="9cd97-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="9cd97-143">เปลี่ยนค่าของฟิลด์ **ขนาดไฟล์สูงสุด** เป็น **51,200**</span><span class="sxs-lookup"><span data-stu-id="9cd97-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="9cd97-144">(ค่าจะแสดงเป็นกิโลไบต์ \[KB\])</span><span class="sxs-lookup"><span data-stu-id="9cd97-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="9cd97-145">เลือก **ตกลง** เพื่อบันทึกการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="9cd97-146">ตั้งค่าคอนฟิกการตั้งค่า Azure</span><span class="sxs-lookup"><span data-stu-id="9cd97-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="9cd97-147">ป้อนรหัสไดเรกทอรี Dataverse และรหัสวัตถุ Azure AD ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9cd97-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="9cd97-148">ป้อนรหัสไดเรกทอรี Dataverse:</span><span class="sxs-lookup"><span data-stu-id="9cd97-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="9cd97-149">เปิด [พอร์ทัล Azure](https://portal.azure.com)</span><span class="sxs-lookup"><span data-stu-id="9cd97-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="9cd97-150">ลงชื่อเข้าใช้โดยใช้รหัสผู้ใช้ที่ใช้ในการสร้างสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="9cd97-151">ไปที่ **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="9cd97-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="9cd97-152">คัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="9cd97-153">ป้อนรหัสวัตถุ Azure Active Directory (Azure AD) ของผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="9cd97-154">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้ไปที่ **ผู้ใช้** และค้นหาผู้ใช้ตามที่อยู่อีเมล</span><span class="sxs-lookup"><span data-stu-id="9cd97-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="9cd97-155">เลือกชื่อของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="9cd97-155">Select the user's name.</span></span>
    3. <span data-ttu-id="9cd97-156">คัดลอกค่า **รหัสวัตถุ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="9cd97-157">ใช้ Azure Cloud Shell เพื่อตั้งค่าทรัพยากร Data Lake ของข้อมูลเชิงลึก Finance</span><span class="sxs-lookup"><span data-stu-id="9cd97-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="9cd97-158">ใช้สคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cd97-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="9cd97-159">มีการให้สคริปต์ Windows PowerShell ไว้ เพื่อให้คุณสามารถตั้งค่าทรัพยากร Azure ที่อธิบายไว้ใน [ตั้งค่าคอนฟิกการส่งออกไปยัง Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) ได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="9cd97-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="9cd97-160">ถ้าคุณต้องการดำเนินการตั้งค่าด้วยตนเอง ให้ข้ามกระบวนงานนี้ และดำเนินการต่อด้วยกระบวนงานในส่วน [การตั้งค่าด้วยตนเอง](#manual-setup)</span><span class="sxs-lookup"><span data-stu-id="9cd97-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="9cd97-161">ทำตามขั้นตอนด้านล่างเพื่อรันสคริปต์ PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cd97-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="9cd97-162">ตัวเลือก Azure CLI "ลอง" หรือการรันสคริปต์บนพีซีของคุณ อาจไม่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="9cd97-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="9cd97-163">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิก Azure โดยใช้สคริปต์ Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cd97-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="9cd97-164">คุณต้องมีสิทธิ์ในการสร้างกลุ่มทรัพยากร Azure ทรัพยากร Azure และแอปพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="9cd97-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="9cd97-165">สำหรับข้อมูลเกี่ยวกับสิทธิ์ที่จำเป็น ให้ดูที่ [ตรวจสอบสิทธิ์ Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app)</span><span class="sxs-lookup"><span data-stu-id="9cd97-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="9cd97-166">ใน [พอร์ทัล azure](https://portal.azure.com) ให้ไปที่การบอกรับเป็นสมาชิก Azure เป้าหมายของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="9cd97-167">เลือกปุ่ม **Cloud Shell** ทางด้านขวาของฟิลด์ **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="9cd97-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="9cd97-168">เลือก **PowerShell**</span><span class="sxs-lookup"><span data-stu-id="9cd97-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="9cd97-169">สร้างที่เก็บข้อมูล ถ้าคุณได้รับพร้อมท์ให้ดำเนินการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="9cd97-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="9cd97-170">ไปที่แท็บ **Azure CLI** และเลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="9cd97-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="9cd97-171">เปิด Notepad และวางสคริปต์ PowerShell</span><span class="sxs-lookup"><span data-stu-id="9cd97-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="9cd97-172">บันทึกไฟล์เป็น ConfigureDataLake.ps1</span><span class="sxs-lookup"><span data-stu-id="9cd97-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="9cd97-173">อัพโหลดสคริปต์ Windows PowerShell ไปยังรอบเวลาโดยใช้ตัวเลือกเมนูเพื่ออัพโหลดใน Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="9cd97-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="9cd97-174">รันสคริปต์ .\ConfigureDataLake.ps1</span><span class="sxs-lookup"><span data-stu-id="9cd97-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="9cd97-175">ติดตามพร้อมท์เพื่อรันสคริปต์</span><span class="sxs-lookup"><span data-stu-id="9cd97-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="9cd97-176">ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อติดตั้ง add-in **ส่งออกไปยัง Data Lake** ใน LCS</span><span class="sxs-lookup"><span data-stu-id="9cd97-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="9cd97-177">ใช้ข้อมูลจากเอาต์พุตของสคริปต์เพื่อเปิดใช้งานที่จัดเก็บเอนทิตีบนหน้า **การเชื่อมต่อข้อมูล** ใน Finance (**การจัดการระบบ \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**)</span><span class="sxs-lookup"><span data-stu-id="9cd97-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="9cd97-178">การตั้งค่าด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="9cd97-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="9cd97-179">เพิ่มแอปพลิเคชันในผู้เช่า Azure AD</span><span class="sxs-lookup"><span data-stu-id="9cd97-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="9cd97-180">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory**</span><span class="sxs-lookup"><span data-stu-id="9cd97-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="9cd97-181">เลือก **จัดการ \> แอปพลิเคชันองค์กร**</span><span class="sxs-lookup"><span data-stu-id="9cd97-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="9cd97-182">ค้นหาแอปพลิเคชันต่อไปนี้ตามรหัสของแอป</span><span class="sxs-lookup"><span data-stu-id="9cd97-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="9cd97-183">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="9cd97-183">Application</span></span>                              | <span data-ttu-id="9cd97-184">รหัสแอพ</span><span class="sxs-lookup"><span data-stu-id="9cd97-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="9cd97-185">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="9cd97-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="9cd97-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="9cd97-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="9cd97-187">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="9cd97-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="9cd97-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="9cd97-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="9cd97-189">บริการตรวจสอบ AI Builder</span><span class="sxs-lookup"><span data-stu-id="9cd97-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="9cd97-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="9cd97-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="9cd97-191">ถ้าคุณไม่พบแอปพลิเคชันก่อนหน้าใดๆ ให้ลองทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="9cd97-192">บนเครื่องเฉพาะที่ของคุณ ให้เลือกเมนู **เริ่มต้น** และค้นหา **powershell**</span><span class="sxs-lookup"><span data-stu-id="9cd97-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="9cd97-193">เลือกและกดค้างไว้ (หรือคลิกขวา) **Windows PowerShell** และจากนั้น เลือก **เรียกใช้ในฐานะผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="9cd97-194">รันคำสั่งต่อไปนี้เพื่อติดตั้งโมดูล **AzureAD**</span><span class="sxs-lookup"><span data-stu-id="9cd97-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="9cd97-195">ถ้าต้องการให้ผู้ให้บริการ NuGet ดำเนินการต่อ ให้เลือก **Y** เพื่อติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="9cd97-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="9cd97-196">ถ้ามีข้อความ "ที่เก็บที่ไม่น่าเชื่อถือ" ปรากฏขึ้น ให้เลือก **Y** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="9cd97-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="9cd97-197">สำหรับแต่ละแอปพลิเคชันที่ต้องมีการเพิ่ม ให้รันคำสั่งต่อไปนี้เพื่อเพิ่มแอปพลิเคชันไปยัง Azure AD</span><span class="sxs-lookup"><span data-stu-id="9cd97-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="9cd97-198">เมื่อคุณได้รับพร้อมท์ ให้ลงชื่อเข้าใช้ในฐานะผู้ดูแลระบบ Azure AD</span><span class="sxs-lookup"><span data-stu-id="9cd97-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="9cd97-199">สร้างแหล่งข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="9cd97-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="9cd97-200">ตรวจสอบให้แน่ใจว่าคุณได้สร้างทรัพยากรต่อไปนี้ในอินสแตนซ์ Azure AD ที่เหมือนกันกับสภาพแวดล้อม Dataverse</span><span class="sxs-lookup"><span data-stu-id="9cd97-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="9cd97-201">คุณไม่สามารถใช้ทรัพยากรจากอินสแตนซ์ Azure AD อื่นได้</span><span class="sxs-lookup"><span data-stu-id="9cd97-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="9cd97-202">การสร้างบัญชีที่จัดเก็บใหม่:</span><span class="sxs-lookup"><span data-stu-id="9cd97-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="9cd97-203">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้างบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="9cd97-204">ในกล่องโต้ตอบ **สร้างบัญชีที่จัดเก็บ** ให้ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="9cd97-205">**สถานที่** – เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="9cd97-206">**ประสิทธิภาพ** – เราขอแนะนำให้คุณเลือก **มาตรฐาน**</span><span class="sxs-lookup"><span data-stu-id="9cd97-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="9cd97-207">**ชนิดบัญชี** – คุณต้องเลือก **StorageV2**</span><span class="sxs-lookup"><span data-stu-id="9cd97-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="9cd97-208">ในกล่องโต้ตอบ **ตัวเลือกขั้นสูง** สำหรับตัวเลือก **Data Lake storage Gen2** เลือก **เปิดใช้งาน** ภายใต้คุณลักษณะ **namespaces ตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="9cd97-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="9cd97-209">ถ้าคุณปิดใช้งานคุณลักษณะนี้ คุณไม่สามารถใช้ข้อมูลที่แอป Finance and Operations เขียนโดยใช้บริการต่างๆ เช่น โฟลว์ข้อมูล Power BI</span><span class="sxs-lookup"><span data-stu-id="9cd97-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="9cd97-210">เลือก **รีวิวและสร้าง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-210">Select **Review and create**.</span></span> <span data-ttu-id="9cd97-211">เมื่อการปรับใช้งานเสร็จสมบูรณ์ จะมีการแสดงทรัพยากรใหม่ในพอร์ทัล Azure</span><span class="sxs-lookup"><span data-stu-id="9cd97-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="9cd97-212">ไปที่บัญชีจัดเก็บข้อมูลที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="9cd97-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="9cd97-213">บนเมนูด้านซ้าย ให้เลือก **คีย์การเข้าถึง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="9cd97-214">คัดลอกและบันทึกสตริงการเชื่อมต่อสำหรับ **คีย์1** หรือ **คีย์2** อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="9cd97-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="9cd97-215">คัดลอกและบันทึกชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="9cd97-216">สร้าง Key Vault ใหม่:</span><span class="sxs-lookup"><span data-stu-id="9cd97-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="9cd97-217">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้สร้าง Key Vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="9cd97-218">ในกล่องโต้ตอบ **สร้าง Key Vault** ในฟิลด์ **สถานที่** ให้เลือกศูนย์ข้อมูลที่เป็นที่ตั้งของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="9cd97-219">หลังจากที่มีการสร้าง Key Vault แล้ว ให้เลือกในรายการ แล้วจากนั้น เลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="9cd97-220">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="9cd97-221">ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="9cd97-222">ป้อนชื่อสำหรับข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="9cd97-222">Enter a name for the secret.</span></span> <span data-ttu-id="9cd97-223">ให้จดบันทึกชื่อ เนื่องจากคุณจะต้องระบุชื่อนี้ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="9cd97-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="9cd97-224">ในฟิลด์ **ค่า** ให้ป้อนสตริงการเชื่อมต่อที่คุณได้รับจากบัญชีที่จัดเก็บในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="9cd97-225">เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="9cd97-226">ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="9cd97-227">ไปที่ **ภาพรวมของ Key Vault** และจดบันทึกชื่อของ DNS</span><span class="sxs-lookup"><span data-stu-id="9cd97-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="9cd97-228">สร้างและลงทะเบียนแอปพลิเคชัน Azure AD:</span><span class="sxs-lookup"><span data-stu-id="9cd97-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="9cd97-229">ใน [พอร์ทัล Azure](https://portal.azure.com) ไปยัง **Azure Active Directory** แล้วจากนั้น เลือก **การลงทะเบียนแอป**</span><span class="sxs-lookup"><span data-stu-id="9cd97-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="9cd97-230">เลือก **การลงทะเบียนแอปพลิเคชันใหม่** และตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="9cd97-231">**ชื่อ** – ป้อนชื่อของแอป</span><span class="sxs-lookup"><span data-stu-id="9cd97-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="9cd97-232">**ชนิดของแอปพลิเคชัน** – เลือก **Web API**</span><span class="sxs-lookup"><span data-stu-id="9cd97-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="9cd97-233">**เปลี่ยนเส้นทางการตั้งค่า URI** – ป้อน URL สำหรับอินสแตนซ์ Dynamics 365 ของคุณ เช่น `https://yourdynamicsinstance.dynamics.com/auth`</span><span class="sxs-lookup"><span data-stu-id="9cd97-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="9cd97-234">ไปที่แอปพลิเคชันที่คุณเพิ่งสร้างขึ้น และคัดลอกและบันทึกค่า **รหัสของแอปพลิเคชัน (ไคลเอนต์)**</span><span class="sxs-lookup"><span data-stu-id="9cd97-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="9cd97-235">คุณจะต้องระบุค่านี้ในภายหลัง เมื่อคุณตั้งค่า key vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="9cd97-236">ไปที่ **สิทธิ์ของ API** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="9cd97-237">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="9cd97-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="9cd97-238">เลือก **Azure Key Vault**</span><span class="sxs-lookup"><span data-stu-id="9cd97-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="9cd97-239">หลังจากที่คุณเลือกสิทธิ์ที่ได้รับมอบหมาย ให้เลือก **ผู้ใช้\_การเลียนแบบ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="9cd97-240">เลือก **เพิ่มสิทธิ์**</span><span class="sxs-lookup"><span data-stu-id="9cd97-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="9cd97-241">บนเมนูสำหรับแอป ให้เลือก **ใบรับรอง \& ข้อมูลลับ** และจากนั้น ทำตามขั้นตอนต่อไปนี้เพื่อสร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="9cd97-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="9cd97-242">เลือก **ข้อมูลลับของไคลเอนต์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9cd97-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="9cd97-243">ในฟิลด์ **คำอธิบาย Key** ให้ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="9cd97-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="9cd97-244">เลือกระยะเวลา แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9cd97-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="9cd97-245">ข้อมูลลับจะถูกสร้างขึ้นในฟิลด์ **ค่า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="9cd97-246">คัดลอกและบันทึกค่าลับ</span><span class="sxs-lookup"><span data-stu-id="9cd97-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="9cd97-247">สร้างข้อมูลลับของ Key Vault:</span><span class="sxs-lookup"><span data-stu-id="9cd97-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="9cd97-248">ไปที่ Key Vault ที่คุณสร้างไว้ก่อนหน้านี้ และเลือก **ข้อมูลลับ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="9cd97-249">สำหรับชื่อลับแต่ละชื่อในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9cd97-250">เลือก **สร้าง/นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="9cd97-251">ในกล่องโต้ตอบ **สร้างข้อมูลลับ** ในฟิลด์ **ตัวเลือกการอัปโหลด** ให้เลือก **ด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="9cd97-252">สร้างชื่อและค่าลับจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="9cd97-253">เลือก **เปิดใช้งานแล้ว** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="9cd97-254">ข้อมูลลับจะถูกสร้างขึ้นและเพิ่มเข้าไปใน Key Vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="9cd97-255">ชื่อข้อมูลลับ</span><span class="sxs-lookup"><span data-stu-id="9cd97-255">Secret name</span></span>                       | <span data-ttu-id="9cd97-256">ค่าลับ</span><span class="sxs-lookup"><span data-stu-id="9cd97-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="9cd97-257">รหัสแอป</span><span class="sxs-lookup"><span data-stu-id="9cd97-257">app-id</span></span>                            | <span data-ttu-id="9cd97-258">รหัสแอปของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="9cd97-259">ข้อมูลลับของแอป</span><span class="sxs-lookup"><span data-stu-id="9cd97-259">app-secret</span></span>                        | <span data-ttu-id="9cd97-260">ความลับของไคลเอนต์ที่คุณบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="9cd97-261">ชื่อบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-261">storage-account-name</span></span>              | <span data-ttu-id="9cd97-262">ชื่อของบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้ เช่น **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="9cd97-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="9cd97-263">สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-263">storage-account-connection-string</span></span> | <span data-ttu-id="9cd97-264">สตริงการเชื่อมต่อที่คุณคัดลอกมาจากหน้า **คีย์การเข้าถึง** สำหรับบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="9cd97-265">อนุญาตให้แอปพลิเคชันเข้าถึง key vault:</span><span class="sxs-lookup"><span data-stu-id="9cd97-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="9cd97-266">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิด key vault ที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="9cd97-267">เลือกนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9cd97-267">Select the access policies.</span></span>
    3. <span data-ttu-id="9cd97-268">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9cd97-269">เลือก **เพิ่มนโยบายการเข้าถึง** เพื่อสร้างนโยบายการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="9cd97-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="9cd97-270">ในฟิลด์ **สิทธิ์ของข้อมูลลับ** ให้เลือกสิทธิ์จากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="9cd97-271">ในฟิลด์ **หลักการเลือก** ให้ค้นหาชื่อที่แสดงของแอปพลิเคชันจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="9cd97-272">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="9cd97-272">Select **Select**.</span></span>
        5. <span data-ttu-id="9cd97-273">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="9cd97-273">Select **Add**.</span></span>
        6. <span data-ttu-id="9cd97-274">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9cd97-274">Select **Save**.</span></span>

        | <span data-ttu-id="9cd97-275">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="9cd97-275">Application</span></span>                                              | <span data-ttu-id="9cd97-276">สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="9cd97-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="9cd97-277">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9cd97-277">The display name of the new application that you created</span></span> | <span data-ttu-id="9cd97-278">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="9cd97-278">Get, List</span></span>   |
        | <span data-ttu-id="9cd97-279">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="9cd97-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="9cd97-280">เรียกดู รายการ</span><span class="sxs-lookup"><span data-stu-id="9cd97-280">Get, List</span></span>   |

6. <span data-ttu-id="9cd97-281">กำหนดบทบาทที่จะเข้าถึงบัญชีที่จัดเก็บ:</span><span class="sxs-lookup"><span data-stu-id="9cd97-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="9cd97-282">ใน [พอร์ทัล Azure](https://portal.azure.com) ให้เปิดบัญชีที่จัดเก็บที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="9cd97-283">เลือก **การควบคุมการเข้าถึง (IAM)** และจากนั้น เลือก **การกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="9cd97-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="9cd97-284">เลือก **เพิ่ม เพิ่มการกำหนดบทบาท**</span><span class="sxs-lookup"><span data-stu-id="9cd97-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="9cd97-285">สำหรับแต่ละแอปพลิเคชันในตารางต่อไปนี้ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9cd97-286">เลือกบทบาทจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="9cd97-287">ปล่อยฟิลด์ **กำหนดการเข้าถึงแก่** ให้มีการตั้งค่าเป็น **ผู้ใช้ กลุ่ม หรือผู้ใช้งานบริการ Azure AD**</span><span class="sxs-lookup"><span data-stu-id="9cd97-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="9cd97-288">ในฟิลด์ **เลือก** ให้ป้อนแอปพลิเคชันจากตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="9cd97-289">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9cd97-289">Select **Save**.</span></span>

        | <span data-ttu-id="9cd97-290">ใบคำขอเปิด</span><span class="sxs-lookup"><span data-stu-id="9cd97-290">Application</span></span>                                              | <span data-ttu-id="9cd97-291">บทบาท</span><span class="sxs-lookup"><span data-stu-id="9cd97-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="9cd97-292">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9cd97-292">The display name of the new application that you created</span></span> | <span data-ttu-id="9cd97-293">เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="9cd97-293">Owner</span></span>                       |
        | <span data-ttu-id="9cd97-294">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9cd97-294">The display name of the new application that you created</span></span> | <span data-ttu-id="9cd97-295">ผู้จ่ายสมทบ</span><span class="sxs-lookup"><span data-stu-id="9cd97-295">Contributor</span></span>                 |
        | <span data-ttu-id="9cd97-296">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9cd97-296">The display name of the new application that you created</span></span> | <span data-ttu-id="9cd97-297">ผู้สนับสนุนบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="9cd97-298">ชื่อที่แสดงของแอปพลิเคชันใหม่ที่คุณสร้าง</span><span class="sxs-lookup"><span data-stu-id="9cd97-298">The display name of the new application that you created</span></span> | <span data-ttu-id="9cd97-299">เจ้าของข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="9cd97-300">**บริการตรวจสอบ AI Builder**</span><span class="sxs-lookup"><span data-stu-id="9cd97-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="9cd97-301">ตัวอ่านข้อมูล Blob ที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="9cd97-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="9cd97-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="9cd97-303">ตั้งค่าคอนฟิก data lake</span><span class="sxs-lookup"><span data-stu-id="9cd97-303">Configure the data lake</span></span>

<span data-ttu-id="9cd97-304">ทำตามขั้นตอนต่อไปนี้เพื่อใช้ LCS เพื่อเพิ่ม add-in ของ Azure Data Lake ไปยังสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="9cd97-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="9cd97-305">ลงชื่อเข้าใช้ LCS แล้วจากนั้นภายใต้ชื่อสภาพแวดล้อมทางด้านขวาของหน้า ให้เลือก **รายละเอียดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9cd97-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="9cd97-306">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="9cd97-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="9cd97-307">เลือก add-in **ส่งออกไปยัง Data Lake**</span><span class="sxs-lookup"><span data-stu-id="9cd97-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="9cd97-308">ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-308">Enter the following values.</span></span>

    | <span data-ttu-id="9cd97-309">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="9cd97-309">Value</span></span>                                                              | <span data-ttu-id="9cd97-310">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9cd97-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="9cd97-311">รหัสผู้เช่าของการบอกรับเป็นสมาชิก Azure ที่เป็นที่ตั้งของ Key Vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="9cd97-312">รหัสผู้เช่าซึ่งเป็นที่ตั้งของบัญชีที่จัดเก็บ แอป และ Key Vault</span><span class="sxs-lookup"><span data-stu-id="9cd97-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="9cd97-313">เมื่อต้องการค้นหาค่านี้ ให้เปิด [พอร์ทัล Azure](https://portal.azure.com) ไปที่ **Azure Active Directory** และคัดลอกค่า **รหัสผู้เช่า**</span><span class="sxs-lookup"><span data-stu-id="9cd97-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="9cd97-314">ระบุชื่อ DNS ของ Key Vault ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="9cd97-315">ชื่อ DNS ของ Key Vault เช่น `https://customkeyvault.vault.azure.net/`</span><span class="sxs-lookup"><span data-stu-id="9cd97-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="9cd97-316">(ค่านี้จะตรงกับชื่อ DNS ที่ใช้ในที่จัดเก็บเอนทิตี)</span><span class="sxs-lookup"><span data-stu-id="9cd97-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="9cd97-317">ระบุข้อมูลลับที่มีชื่อของบัญชีที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="9cd97-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="9cd97-318">**ชื่อ-บัญชี-ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="9cd97-319">ชื่อลับสำหรับรหัสแอปที่จะใช้สำหรับการเข้าถึง Data Lake</span><span class="sxs-lookup"><span data-stu-id="9cd97-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="9cd97-320">**รหัส-แอป**</span><span class="sxs-lookup"><span data-stu-id="9cd97-320">**app-id**</span></span> |
    | <span data-ttu-id="9cd97-321">ชื่อลับที่จะใช้กับรหัสแอป</span><span class="sxs-lookup"><span data-stu-id="9cd97-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="9cd97-322">**ข้อมูลลับ-แอป**</span><span class="sxs-lookup"><span data-stu-id="9cd97-322">**app-secret**</span></span> |

5. <span data-ttu-id="9cd97-323">ยอมรับเงื่อนไข และเลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="9cd97-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="9cd97-324">จะมีการติดตั้ง add-in ภายในสองสามนาที</span><span class="sxs-lookup"><span data-stu-id="9cd97-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="9cd97-325">ตั้งค่าคอนฟิก AI Builder</span><span class="sxs-lookup"><span data-stu-id="9cd97-325">Configure AI Builder</span></span>

1. <span data-ttu-id="9cd97-326">ลงชื่อเข้าใช้ LCS และเปิดหน้า **รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="9cd97-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="9cd97-327">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="9cd97-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="9cd97-328">คุณควรเห็น add-in ที่ติดตั้งอยู่แล้วในสภาพแวดล้อมนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="9cd97-329">ถ้า add-in **ส่งออกไปยัง Data Lake** ไม่ได้อยู่ในนั้น ตั้งค่าคอนฟิก add-in นี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="9cd97-330">เลือก add-in **รับข้อมูลเชิงลึก**</span><span class="sxs-lookup"><span data-stu-id="9cd97-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="9cd97-331">บนหน้ารายละเอียด add-in  **รับข้อมูลเชิงลึก** ให้ป้อนค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="9cd97-332">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="9cd97-332">Value</span></span>                                                    | <span data-ttu-id="9cd97-333">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="9cd97-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="9cd97-334">URL ขององค์กร CDS</span><span class="sxs-lookup"><span data-stu-id="9cd97-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="9cd97-335">URL ขององค์กรของ Dataverse ถูกคัดลอกจากด้านบน</span><span class="sxs-lookup"><span data-stu-id="9cd97-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="9cd97-336">รหัสองค์กร CDS</span><span class="sxs-lookup"><span data-stu-id="9cd97-336">CDS Org ID</span></span>                                               | <span data-ttu-id="9cd97-337">ID ขององค์กรของ Dataverse ถูกคัดลอกจากด้านบน</span><span class="sxs-lookup"><span data-stu-id="9cd97-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="9cd97-338">เปิดใช้งาน **นี่เป็นสภาพแวดล้อมเริ่มต้นสำหรับผู้เช่าของคุณหรือไม่**</span><span class="sxs-lookup"><span data-stu-id="9cd97-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="9cd97-339">ตั้งค่าคอนฟิกที่จัดเก็บเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="9cd97-339">Configure the entity store</span></span>

<span data-ttu-id="9cd97-340">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าที่จัดเก็บเอนทิตีในสภาพแวดล้อมทาง Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="9cd97-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="9cd97-341">ไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ระบบ \> การเชื่อมต่อข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9cd97-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="9cd97-342">ตั้งค่าฟิลด์ Key Vault ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9cd97-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="9cd97-343">**รหัสแอปพลิเคชัน (ไคลเอนต์)** – ป้อนรหัสไคลเอนต์ของแอแพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="9cd97-344">**ข้อมูลลับของแอปพลิเคชัน** – ป้อนข้อมูลลับที่คุณบันทึกไว้สำหรับแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="9cd97-345">**ชื่อ DNS** – คุณสามารถค้นหาชื่อของ Domain Name System (DNS) บนหน้ารายละเอียดของแอปพลิเคชันที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="9cd97-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="9cd97-346">**ชื่อลับ** – ป้อน **สตริง-การเชื่อมต่อ-บัญชี-ที่จัดเก็บ**</span><span class="sxs-lookup"><span data-stu-id="9cd97-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="9cd97-347">เปิดใช้งาน **เปิดใช้งานการรวม Data Lake**</span><span class="sxs-lookup"><span data-stu-id="9cd97-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="9cd97-348">เลือก **ทดสอบ Azure Key Vault** และตรวจสอบว่าไม่มีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9cd97-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="9cd97-349">เลือก **การจัดเก็บ Test Azure** และตรวจสอบว่าไม่มีข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="9cd97-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="9cd97-350">ผลป้อนกลับและการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="9cd97-350">Feedback and support</span></span>

<span data-ttu-id="9cd97-351">โปรดส่งอีเมล์ถึง [ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง)](mailto:fiap@microsoft.com) หากคุณมีความสนใจในการให้ผลป้อนกลับหรือต้องการความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="9cd97-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="9cd97-352">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="9cd97-352">Privacy notice</span></span>

<span data-ttu-id="9cd97-353">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="9cd97-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
