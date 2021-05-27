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
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017017"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="8eec8-103">Add-in การมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="8eec8-104">Add-in การมองเห็นสินค้าคงคลังเป็น microservice อิสระและปรับสเกลได้อย่างมาก ซึ่งเปิดใช้งานการติดตามปริมาณคงคลังคงเหลือในเวลาจริง จึงให้มุมมองส่วนกลางของการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="8eec8-105">ข้อมูลทั้งหมดที่เกี่ยวข้องกับปริมาณคงคลังคงเหลือจะถูกส่งออกไปยังบริการใกล้เคียงเวลาจริงผ่านการรวม SQL ในระดับต่ำ</span><span class="sxs-lookup"><span data-stu-id="8eec8-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="8eec8-106">ระบบภายนอกเข้าถึงบริการผ่าน RESTful APIs เพื่อสอบถามข้อมูลปริมาณคงคลังคงเหลือในชุดของมิติที่กำหนด ดังนั้นจึงดึงข้อมูลรายการของตำแหน่งในปริมาณคงคลังคงเหลือที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8eec8-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="8eec8-107">การแสดงผลสินค้าคงคลังเป็น microservice ที่สร้างขึ้นบน Microsoft Dataverse ซึ่งหมายความว่า คุณสามารถขยายได้โดยการสร้าง Power Apps และการใช้ Power BI เพื่อให้ฟังก์ชันการทำงานที่กำหนดเองตรงกับความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="8eec8-108">นอกจากนี้ คุณยังสามารถอัปเกรดดัชนีเพื่อทำการสอบถามสินค้าคงคลังได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8eec8-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="8eec8-109">ความสามารถในการมองเห็นสินค้าคงคลังจะให้ตัวเลือกการตั้งค่าคอนฟิกซึ่งช่วยให้สามารถรวมกับระบบต่างๆ ของบุคคลที่สามได้</span><span class="sxs-lookup"><span data-stu-id="8eec8-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="8eec8-110">ซึ่งสนับสนุนมิติสินค้าคงคลังมาตรฐาน ความสามารถที่กำหนดเอง และปริมาณที่มีการคำนวณซึ่งสามารถตั้งค่าคอนฟิกได้แบบมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="8eec8-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="8eec8-111">หัวข้อนี้จะอธิบายวิธีการติดตั้งและตั้งค่าคอนฟิก Add-in ความสามารถในการมองเห็นสินค้าคงคลังสำหรับ Dynamics 365 Supply Chain Management และวิธีใช้ Application Programming Interface (API)</span><span class="sxs-lookup"><span data-stu-id="8eec8-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="8eec8-112">ติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="8eec8-113">คุณจำเป็นต้องติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลังโดยใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8eec8-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8eec8-114">LCS เป็นพอร์ทัลการทำงานร่วมกันที่ให้สภาพแวดล้อมและชุดของบริการที่อัปเดตเป็นประจำ ซึ่งช่วยให้คุณสามารถจัดการวงจรการใช้งานแอปพลิเคชันของแอป Dynamics 365 Finance and Operations ของคุณได้</span><span class="sxs-lookup"><span data-stu-id="8eec8-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="8eec8-115">สำหรับข้อมูลเพิ่มเติม ให้ดู [ทรัพยากร Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)</span><span class="sxs-lookup"><span data-stu-id="8eec8-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="8eec8-116">ข้อกำหนดเบื้องต้นของ Add-in การแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="8eec8-117">ก่อนที่คุณจะสามารถติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง คุณต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="8eec8-118">รับโครงการสำหรับการใช้งาน LCS โดยมีสภาพแวดล้อมที่ปรับใช้อย่างน้อยหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="8eec8-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="8eec8-119">โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่า Add-in ของข้อกำหนดเบื้องต้น ใน [ภาพรวมของ Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="8eec8-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="8eec8-120">Inventory Visibility ไม่ต้องการการเชื่อมโยงแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="8eec8-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="8eec8-121">ติดต่อ Inventory Visibility Team ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์ที่ต้องการสามไฟล์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="8eec8-122">`Inventory Visibility Integration.zip` (ถ้าเวอร์ชันของ Supply Chain Management ที่คุณรันอยู่เป็นรุ่นก่อนหน้าเวอร์ชัน 10.0.18)</span><span class="sxs-lookup"><span data-stu-id="8eec8-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="8eec8-123">หรือติดต่อ Inventory Visibility Team ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับแพคเกจ Package Deployer</span><span class="sxs-lookup"><span data-stu-id="8eec8-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="8eec8-124">แพคเกจเหล่านี้สามารถใช้ได้โดยเครื่องมือ Package Deployer ทางการ</span><span class="sxs-lookup"><span data-stu-id="8eec8-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="8eec8-125">`InventoryServiceApplication.PackageDeployer.zip` (แพคเกจนี้จะมีการเปลี่ยนแปลงทั้งหมดในแพคเกจ `InventoryServiceBase` บวกส่วนประกอบของแอปพลิเคชัน UI เพิ่มเติม)</span><span class="sxs-lookup"><span data-stu-id="8eec8-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="8eec8-126">ปฏิบัติตามคําแนะนําที่แนะนําใน [การเริ่มต้นแบบด่วน: ลงทะเบียนแอพลิเคชันด้วยแพลตฟอร์มข้อมูลเฉพาะตัวของ Microsoft](/azure/active-directory/develop/quickstart-register-app) เพื่อลงทะเบียนแอปพลิเคชันและเพิ่มข้อมูลลับของไคลเอนต์ลงใน AAD ภายใต้การบอกรับเป็นสมาชิก Azure ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="8eec8-127">ลงทะเบียนแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="8eec8-128">เพิ่มข้อมูลลับไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="8eec8-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="8eec8-129">รหัส **รหัสแอปพลิเคชัน (ไคลเอนต์)** **ข้อมูลลับไคลเอนต์** และ **รหัสผู้เช่า** จะใช้ในขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="8eec8-130">ประเทศและภูมิภาคที่ได้รับการสนับสนุนในปัจจุบัน ได้แก่ แคนาดา สหรัฐอเมริกา และสหภาพยุโรป (EU)</span><span class="sxs-lookup"><span data-stu-id="8eec8-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="8eec8-131">ถ้าคุณมีคำถามใดๆ เกี่ยวกับข้อกำหนดเบื้องต้นเหล่านี้ โปรดติดต่อทีมงานผลิตภัณฑ์ของความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="8eec8-132">ตั้งค่า Dataverse</span><span class="sxs-lookup"><span data-stu-id="8eec8-132">Set up Dataverse</span></span>

<span data-ttu-id="8eec8-133">หากต้องการตั้งค่า Dataverse สำหรับใช้งานกับความสามารถในการมองเห็นสินค้าคงคลัง คุณต้องจัดเตรียมเงื่อนไขเบื้องต้นก่อน แล้วจึงตัดสินใจว่าจะตั้งค่า Dataverse โดยใช้เครื่องมือ Package Deployer หรือนําเข้าโซลูชันด้วยตนเอง (คุณไม่ต้องติดตั้งทั้งสองอย่าง)</span><span class="sxs-lookup"><span data-stu-id="8eec8-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="8eec8-134">จากนั้นติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="8eec8-135">ส่วนย่อยต่อไปนี้อธิบายถึงวิธีทำงานเหล่านี้แต่ละรายการให้เสร็จ</span><span class="sxs-lookup"><span data-stu-id="8eec8-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="8eec8-136">จัดเตรียมข้อกำหนดเบื้องต้นของ Dataverse</span><span class="sxs-lookup"><span data-stu-id="8eec8-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="8eec8-137">ก่อนที่คุณจะเริ่มตั้งค่า Dataverse ให้เพิ่มหลักการบริการเข้าในผู้เช่าของคุณโดยเลือก</span><span class="sxs-lookup"><span data-stu-id="8eec8-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="8eec8-138">ติดตั้ง Azure AD PowerShell Module v2 ตามที่อธิบายไว้ใน [ติดตั้ง Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2)</span><span class="sxs-lookup"><span data-stu-id="8eec8-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="8eec8-139">โดยรันคำสั่ง PowerShell ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="8eec8-140">ตั้งค่า Dataverse โดยใช้เครื่องมือ Package Deployer</span><span class="sxs-lookup"><span data-stu-id="8eec8-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="8eec8-141">หลังจากที่คุณมีข้อกำหนดเบื้องต้นแล้ว ให้ใช้ขั้นตอนต่อไปนี้ถ้าคุณต้องการตั้งค่า Dataverse โดยใช้เครื่องมือ Package Deployer</span><span class="sxs-lookup"><span data-stu-id="8eec8-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="8eec8-142">โปรดดูรายละเอียดในส่วนถัดไปเกี่ยวกับวิธีการนําเข้าโซลูชันด้วยตนเอง (อย่าเลือกทั้งสองอย่าง)</span><span class="sxs-lookup"><span data-stu-id="8eec8-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="8eec8-143">ติดตั้งเครื่องมือของนักพัฒนาตามที่อธิบายไว้ใน [ดาวน์โหลดจาก NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget)</span><span class="sxs-lookup"><span data-stu-id="8eec8-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="8eec8-144">ขึ้นอยู่กับเลือกความต้องการทางธุรกิจของคุณ เลือกแพคเกจ `InventoryServiceBase` หรือ `InventoryServiceApplication`</span><span class="sxs-lookup"><span data-stu-id="8eec8-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="8eec8-145">นำเข้าโซลูชัน:</span><span class="sxs-lookup"><span data-stu-id="8eec8-145">Import the solutions:</span></span>
    1. <span data-ttu-id="8eec8-146">สำหรับแพคเกจ `InventoryServiceBase`:</span><span class="sxs-lookup"><span data-stu-id="8eec8-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="8eec8-147">แตกไฟล์ `InventoryServiceBase.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="8eec8-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="8eec8-148">ค้นหาโฟลเดอร์ `InventoryServiceBase`ไฟล์ `[Content_Types].xml` ไฟล์ `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` ไฟล์ `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` และไฟล์ `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`</span><span class="sxs-lookup"><span data-stu-id="8eec8-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="8eec8-149">คัดลอกโฟลเดอร์และไฟล์เหล่านี้แต่ละไฟล์ไปยังไดเรกทอรี `.\Tools\PackageDeployment` ซึ่งสร้างขึ้นเมื่อคุณติดตั้งเครื่องมือของนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="8eec8-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="8eec8-150">สำหรับแพคเกจ `InventoryServiceApplication`:</span><span class="sxs-lookup"><span data-stu-id="8eec8-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="8eec8-151">แตกไฟล์ `InventoryServiceApplication.PackageDeployer.zip`</span><span class="sxs-lookup"><span data-stu-id="8eec8-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="8eec8-152">ค้นหาโฟลเดอร์ `InventoryServiceApplication`ไฟล์ `[Content_Types].xml` ไฟล์ `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` ไฟล์ `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` และไฟล์ `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`</span><span class="sxs-lookup"><span data-stu-id="8eec8-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="8eec8-153">คัดลอกโฟลเดอร์และไฟล์เหล่านี้แต่ละไฟล์ไปยังไดเรกทอรี `.\Tools\PackageDeployment` ซึ่งสร้างขึ้นเมื่อคุณติดตั้งเครื่องมือของนักพัฒนา</span><span class="sxs-lookup"><span data-stu-id="8eec8-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="8eec8-154">ดำเนินการ `.\Tools\PackageDeployment\PackageDeployer.exe`</span><span class="sxs-lookup"><span data-stu-id="8eec8-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="8eec8-155">ปฏิบัติตามคําแนะนําบนหน้าจอเพื่อนําเข้าโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="8eec8-156">การกำหนดบทบาทความปลอดภัยให้กับผู้ใช้แอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="8eec8-157">เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="8eec8-158">ไปที่ **การตั้งค่าขั้นสูง \> ระบบ \> ความปลอดภัย \> ผู้ใช้** และค้นหาผู้ใช้ที่ชื่อ **# InventoryVisibility**</span><span class="sxs-lookup"><span data-stu-id="8eec8-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="8eec8-159">เลือก **กําหนดบทบาท** แล้วเลือก **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="8eec8-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="8eec8-160">ถ้ามีบทบาทที่มีชื่อ **ผู้ใช้ Common Data Service** ให้เลือกบทบาทนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="8eec8-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="8eec8-161">ตั้งค่า Dataverse ด้วยตนเองโดยการนําเข้าโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="8eec8-162">หลังจากที่คุณมีข้อกำหนดเบื้องต้นแล้ว ให้ใช้ขั้นตอนต่อไปนี้ถ้าคุณต้องการตั้งค่า Dataverse ด้วยตนเองโดยการนําเข้าโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="8eec8-163">โปรดดูรายละเอียดในส่วนก่อนหน้านี้เกี่ยวกับวิธีการใช้เครื่องมือ Package Deployer แทน (อย่าใช้เครื่องมือทั้งสองอย่าง)</span><span class="sxs-lookup"><span data-stu-id="8eec8-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="8eec8-164">สร้างผู้ใช้แอพลิเคชัน สำหรับ Inventory Visibility ใน Dataverse:</span><span class="sxs-lookup"><span data-stu-id="8eec8-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="8eec8-165">เปิด URL ของสภาพแวดล้อม Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="8eec8-166">ไปที่ **การตั้งค่าขั้นสูง \> ระบบ \> ความปลอดภัย \> ผู้ใช้** และสร้างผู้ใช้แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="8eec8-167">ใช้เมนูมุมมองเพื่อเปลี่ยนมุมมองหน้าเป็น **ผู้ใช้แอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="8eec8-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="8eec8-168">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8eec8-168">Select **New**.</span></span> <span data-ttu-id="8eec8-169">ตั้งค่ารหัสแอพลิเคชัน เป็น *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*</span><span class="sxs-lookup"><span data-stu-id="8eec8-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="8eec8-170">(รหัสออบเจ็กต์จะถูกโหลดโดยอัตโนมัติเมื่อคุณบันทึกการเปลี่ยนแปลง) คุณสามารถปรับแต่งชื่อได้</span><span class="sxs-lookup"><span data-stu-id="8eec8-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="8eec8-171">ตัวอย่างเช่น คุณสามารถเปลี่ยนเป็น *Inventory Visibility*</span><span class="sxs-lookup"><span data-stu-id="8eec8-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="8eec8-172">เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8eec8-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="8eec8-173">เลือก **กําหนดบทบาท** แล้วเลือก **ผู้ดูแลระบบ**</span><span class="sxs-lookup"><span data-stu-id="8eec8-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="8eec8-174">ถ้ามีบทบาทที่มีชื่อ **ผู้ใช้ Common Data Service** ให้เลือกบทบาทนั้นด้วย</span><span class="sxs-lookup"><span data-stu-id="8eec8-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="8eec8-175">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างผู้ใช้แอพลิเคชัน](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user)</span><span class="sxs-lookup"><span data-stu-id="8eec8-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="8eec8-176">ถ้าภาษาเริ่มต้นของภาษา Dataverse ของคุณไม่ใช่ **ภาษาอังกฤษ**:</span><span class="sxs-lookup"><span data-stu-id="8eec8-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="8eec8-177">ไปที่ **การตั้งค่าขั้นสูง \> การจัดการ \> ภาษา**</span><span class="sxs-lookup"><span data-stu-id="8eec8-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="8eec8-178">เลือก **ภาษาอังกฤษ (LanguageCode=1033)** และเลือก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="8eec8-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="8eec8-179">นําเข้าไฟล์ `Inventory Visibility Dataverse Solution.zip` ซึ่งประกอบด้วย เอนทิตี้ที่เกี่ยวข้องกับการตั้งค่าคอนฟิก Dataverse และ Power Apps</span><span class="sxs-lookup"><span data-stu-id="8eec8-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="8eec8-180">ไปที่หน้า **โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="8eec8-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="8eec8-181">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="8eec8-181">Select **Import**.</span></span>

1. <span data-ttu-id="8eec8-182">นําเข้าโฟลว์ทริกเกอร์การอัปเกรดการตั้งค่าคอนฟิก:</span><span class="sxs-lookup"><span data-stu-id="8eec8-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="8eec8-183">ไปที่หน้า Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="8eec8-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="8eec8-184">ตรวจสอบให้แน่ใจว่ามีการเชื่อมต่อที่ชื่อ *Dataverse (ดั้งเดิม)* อยู่</span><span class="sxs-lookup"><span data-stu-id="8eec8-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="8eec8-185">(ถ้าไม่มี ให้สร้างใหม่)</span><span class="sxs-lookup"><span data-stu-id="8eec8-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="8eec8-186">นำเข้าไฟล์ `Inventory Visibility Configuration Trigger.zip`</span><span class="sxs-lookup"><span data-stu-id="8eec8-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="8eec8-187">หลังจากนําเข้าแล้ว ทริกเกอร์จะปรากฏขึ้นภายใต้ **โฟลว์ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="8eec8-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="8eec8-188">เริ่มต้นตัวแปรสี่ตัวต่อไปนี้ ตามข้อมูลสภาพแวดล้อม:</span><span class="sxs-lookup"><span data-stu-id="8eec8-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="8eec8-189">รหัสผู้เช่า Azure</span><span class="sxs-lookup"><span data-stu-id="8eec8-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="8eec8-190">รหัสไคลเอนต์แอปพลิเคชัน Azure</span><span class="sxs-lookup"><span data-stu-id="8eec8-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="8eec8-191">ข้อมูลลับไคลเอนต์แอปพลิเคชัน Azure</span><span class="sxs-lookup"><span data-stu-id="8eec8-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="8eec8-192">ปลายทางการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="8eec8-193">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับตัวแปรนี้ โปรดดูที่ส่วน [ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง](#setup-inventory-visibility-integration) ในตอนท้ายของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="8eec8-194">![ทริกเกอร์การตั้งค่าคอนฟิก](media/configuration-trigger.png "ทริกเกอร์การตั้งค่าคอนฟิก")</span><span class="sxs-lookup"><span data-stu-id="8eec8-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="8eec8-195">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="8eec8-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="8eec8-196">ติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="8eec8-196">Install the add-in</span></span>

<span data-ttu-id="8eec8-197">เพื่อติดตั้ง Add-in ความสามารถในการมองเห็นสินค้าคงคลัง ต้องดำเนินการขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="8eec8-198">ลงชื่อเข้าใช้พอร์ทัล [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)</span><span class="sxs-lookup"><span data-stu-id="8eec8-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="8eec8-199">บนโฮมเพจ ให้เลือกโครงการที่มีการปรับใช้สภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="8eec8-200">บนหน้าโครงการ ให้เลือกสภาพแวดล้อมที่คุณต้องการติดตั้ง add-in</span><span class="sxs-lookup"><span data-stu-id="8eec8-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="8eec8-201">ในหน้าสภาพแวดล้อม ให้เลื่อนลงจนกว่าคุณจะเห็นส่วน **Add-in ของสภาพแวดล้อม** ในส่วน **Power Platform การรวม** ที่คุณสามารถค้นหาชื่อสภาพแวดล้อม Dataverse ได้</span><span class="sxs-lookup"><span data-stu-id="8eec8-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="8eec8-202">ในส่วน **add-in สภาพแวดล้อม** ให้เลือก **ติดตั้ง add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8eec8-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="8eec8-203">![หน้าสภาพแวดล้อมใน LCS](media/inventory-visibility-environment.png "หน้าสภาพแวดล้อมใน LCS")</span><span class="sxs-lookup"><span data-stu-id="8eec8-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="8eec8-204">เลือกลิงก์ **ติดตั้ง Add-in ใหม่**</span><span class="sxs-lookup"><span data-stu-id="8eec8-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="8eec8-205">รายการของ add-in ที่พร้อมใช้งานจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="8eec8-206">เลือก **การแสดงผลสินค้าคงคลัง** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="8eec8-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="8eec8-207">ป้อนค่าสำหรับฟิลด์ต่อไปนี้สำหรับสภาพแวดล้อมของคุณ:</span><span class="sxs-lookup"><span data-stu-id="8eec8-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="8eec8-208">**รหัส (ไคลเอนต์) แอปพลิเคชัน AAD**</span><span class="sxs-lookup"><span data-stu-id="8eec8-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="8eec8-209">**รหัสผู้เช่า AAD**</span><span class="sxs-lookup"><span data-stu-id="8eec8-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="8eec8-210">![หน้าการตั้งค่าของ Add in](media/inventory-visibility-setup.png "หน้าการตั้งค่าของ Add in")</span><span class="sxs-lookup"><span data-stu-id="8eec8-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="8eec8-211">ยอมรับข้อกำหนดและเงื่อนไขโดยเลือกกล่องกาเครื่องหมาย **ข้อกำหนดและเงื่อนไข**</span><span class="sxs-lookup"><span data-stu-id="8eec8-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="8eec8-212">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8eec8-212">Select **Install**.</span></span> <span data-ttu-id="8eec8-213">สถานะของ add-in จะแสดงเป็น **กำลังติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8eec8-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="8eec8-214">เมื่อเสร็จสิ้นแล้ว ให้รีเฟรชหน้าเพื่อดูการเปลี่ยนแปลงสถานะเป็น **ติดตั้งแล้ว**</span><span class="sxs-lookup"><span data-stu-id="8eec8-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="8eec8-215">ถอนการติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="8eec8-215">Uninstall the add-in</span></span>

<span data-ttu-id="8eec8-216">เมื่อต้องการถอนการติดตั้ง add-in ให้เลือก **ถอนการติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="8eec8-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="8eec8-217">เมื่อคุณรีเฟรช LCS และ Add-in การแสดงผลสินค้าคงคลังจะถูกลบออก</span><span class="sxs-lookup"><span data-stu-id="8eec8-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="8eec8-218">กระบวนการถอนการติดตั้งจะลบการลงทะเบียน Add-in และยังเริ่มต้นงานเพื่อล้างข้อมูลทางธุรกิจทั้งหมดที่จัดเก็บไว้ในบริการด้วย</span><span class="sxs-lookup"><span data-stu-id="8eec8-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="8eec8-219">ใช้ข้อมูลปริมาณคงคลังคงเหลือจาก Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8eec8-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="8eec8-220">ปรับใช้แพคเกจการรวมการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="8eec8-221">ถ้าคุณรัน Supply Chain Management เวอร์ชัน 10.0.17 หรือก่อนหน้านั้น ให้ติดต่อทีมสนับสนุนการแสดงผลสินค้าคงคลัง ที่ [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) เพื่อรับไฟล์แพคเกจ</span><span class="sxs-lookup"><span data-stu-id="8eec8-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="8eec8-222">แล้วปรับใช้แพคเกจใน LCS</span><span class="sxs-lookup"><span data-stu-id="8eec8-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="8eec8-223">ถ้าเกิดข้อผิดพลาดที่ไม่ตรงกันของเวอร์ชันระหว่างการปรับใช้ คุณต้องนําเข้าโครงการ X++ ด้วยตนเอง ลงในสภาพแวดล้อมการพัฒนาของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="8eec8-224">จากนั้นสร้างแพคเกจที่สามารถปรับใช้งานได้ในสภาพแวดล้อมการพัฒนาของคุณ และปรับใช้ในสภาพแวดล้อมการทำงานจริงของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="8eec8-225">รหัสถูกรวมอยู่กับ Supply Chain Management เวอร์ชัน 10.0.18</span><span class="sxs-lookup"><span data-stu-id="8eec8-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="8eec8-226">ถ้าคุณรันเวอร์ชันนั้นอยู่หรือเวอร์ชันที่ใหม่กว่า ไม่ต้องมีการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="8eec8-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="8eec8-227">ตรวจสอบให้แน่ใจว่าคุณลักษณะต่อไปนี้ได้เปิดใช้งานอยู่ในสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="8eec8-228">(โดยค่าเริ่มต้น จะเปิดใช้งาน)</span><span class="sxs-lookup"><span data-stu-id="8eec8-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="8eec8-229">คำอธิบายลักษณะการทำงาน</span><span class="sxs-lookup"><span data-stu-id="8eec8-229">Feature description</span></span> | <span data-ttu-id="8eec8-230">เวอร์ชันรหัส</span><span class="sxs-lookup"><span data-stu-id="8eec8-230">Code version</span></span> | <span data-ttu-id="8eec8-231">สลับคลาส</span><span class="sxs-lookup"><span data-stu-id="8eec8-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="8eec8-232">เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSum</span><span class="sxs-lookup"><span data-stu-id="8eec8-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="8eec8-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="8eec8-233">10.0.11</span></span> | <span data-ttu-id="8eec8-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="8eec8-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="8eec8-235">เปิดใช้งานหรือปิดใช้งานการใช้มิติสินค้าคงคลังในตาราง InventSumDelta</span><span class="sxs-lookup"><span data-stu-id="8eec8-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="8eec8-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="8eec8-236">10.0.12</span></span> | <span data-ttu-id="8eec8-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="8eec8-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="8eec8-238">ตั้งค่าการรวมการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="8eec8-239">ใน Supply Chain Management ให้เปิดพื้นที่ทำงาน **[การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** และเปิดคุณลักษณะ **การรวมการแสดงผลสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="8eec8-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="8eec8-240">ไปที่ **การจัดการสินค้าคงคลัง \> ตั้งค่า \> พารามิเตอร์การรวมการแสดงผลสินค้าคงคลัง** และป้อน URL ของสภาพแวดล้อมที่คุณรันการแสดงผลสินค้าคงคลังอยู่</span><span class="sxs-lookup"><span data-stu-id="8eec8-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="8eec8-241">ค้นหาภูมิภาค Azure ของสภาพแวดล้อม LCS ของคุณ แล้วป้อน URL</span><span class="sxs-lookup"><span data-stu-id="8eec8-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="8eec8-242">URL มีฟอร์มต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="8eec8-243">ตัวอย่างเช่น ถ้าคุณอยู่ในยุโรป สภาพแวดล้อมของคุณจะมี URL อย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="8eec8-244">ภูมิภาคต่อไปนี้พร้อมใช้งานในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="8eec8-245">ภูมิภาคของ Azure</span><span class="sxs-lookup"><span data-stu-id="8eec8-245">Azure region</span></span> | <span data-ttu-id="8eec8-246">ชื่อย่อของภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="8eec8-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="8eec8-247">ออสเตรเลียตะวันออก</span><span class="sxs-lookup"><span data-stu-id="8eec8-247">Australia east</span></span> | <span data-ttu-id="8eec8-248">eau</span><span class="sxs-lookup"><span data-stu-id="8eec8-248">eau</span></span> |
    | <span data-ttu-id="8eec8-249">ออสเตรเลียตะวันออกเฉียงใต้</span><span class="sxs-lookup"><span data-stu-id="8eec8-249">Australia southeast</span></span> | <span data-ttu-id="8eec8-250">seau</span><span class="sxs-lookup"><span data-stu-id="8eec8-250">seau</span></span> |
    | <span data-ttu-id="8eec8-251">แคนาดากลาง</span><span class="sxs-lookup"><span data-stu-id="8eec8-251">Canada central</span></span> | <span data-ttu-id="8eec8-252">cca</span><span class="sxs-lookup"><span data-stu-id="8eec8-252">cca</span></span> |
    | <span data-ttu-id="8eec8-253">แคนาดาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="8eec8-253">Canada east</span></span> | <span data-ttu-id="8eec8-254">eca</span><span class="sxs-lookup"><span data-stu-id="8eec8-254">eca</span></span> |
    | <span data-ttu-id="8eec8-255">ยุโรปเหนือ</span><span class="sxs-lookup"><span data-stu-id="8eec8-255">North Europe</span></span> | <span data-ttu-id="8eec8-256">neu</span><span class="sxs-lookup"><span data-stu-id="8eec8-256">neu</span></span> |
    | <span data-ttu-id="8eec8-257">ยุโรปตะวันตก</span><span class="sxs-lookup"><span data-stu-id="8eec8-257">West Europe</span></span> | <span data-ttu-id="8eec8-258">weu</span><span class="sxs-lookup"><span data-stu-id="8eec8-258">weu</span></span> |
    | <span data-ttu-id="8eec8-259">สหรัฐอเมริกาตะวันออก</span><span class="sxs-lookup"><span data-stu-id="8eec8-259">East US</span></span> | <span data-ttu-id="8eec8-260">eus</span><span class="sxs-lookup"><span data-stu-id="8eec8-260">eus</span></span> |
    | <span data-ttu-id="8eec8-261">สหรัฐอเมริกาตะวันตก</span><span class="sxs-lookup"><span data-stu-id="8eec8-261">West US</span></span> | <span data-ttu-id="8eec8-262">wus</span><span class="sxs-lookup"><span data-stu-id="8eec8-262">wus</span></span> |

1. <span data-ttu-id="8eec8-263">ไปที่ **การจัดการสินค้าคงคลัง \> ประจำงวด \> การรวมการแสดงผลสินค้าคงคลัง** และเปิดใช้งานงาน</span><span class="sxs-lookup"><span data-stu-id="8eec8-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="8eec8-264">ขณะนี้เหตุการณ์การเปลี่ยนแปลงสินค้าคงคลังทั้งหมดจาก Supply Chain Management จะถูกลงรายการบัญชีไปยังการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="8eec8-265">API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="8eec8-266">REST API สาธารณะของ Add-in การแสดงผลสินค้าคงคลัง แสดงถึงปลายทางเฉพาะสำหรับการรวมหลายแห่ง</span><span class="sxs-lookup"><span data-stu-id="8eec8-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="8eec8-267">ซึ่งสนับสนุนชนิดการโต้ตอบหลักสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="8eec8-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="8eec8-268">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปที่ add-in จากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8eec8-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="8eec8-269">การสอบถามปริมาณคงคลังคงเหลือปัจจุบันจากระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8eec8-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="8eec8-270">การซิงโครไนส์อัตโนมัติกับ Supply Chain Management สินค้าคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8eec8-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="8eec8-271">การซิงโครไนส์อัตโนมัติไม่ได้เป็นส่วนหนึ่งของ API สาธารณะ</span><span class="sxs-lookup"><span data-stu-id="8eec8-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="8eec8-272">แต่จะถูกจัดการในพื้นหลังของสภาพแวดล้อมซึ่งเปิดใช้งาน Add-in ของการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="8eec8-273">การรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8eec8-273">Authentication</span></span>

<span data-ttu-id="8eec8-274">โทเคนความปลอดภัยของแพลตฟอร์มจะใช้ในการเรียก Add-in ของการแสดงผลสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="8eec8-275">ดังนั้น คุณจึงต้องสร้างโทเคน *Azure Active Directory (Azure AD)* โดยใช้แอพลิเคชัน Azure AD ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="8eec8-276">จากนั้นคุณต้องใช้โทเคน Azure AD เพื่อรับ *การเข้าถึงโทเคน* จากบริการความปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="8eec8-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="8eec8-277">รับโทเคนบริการรักษาความปลอดภัย โดยทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="8eec8-278">ล็อกอินเข้าสู่พอร์ทัล Azure และใช้งาน เพื่อค้นหา `clientId` และ `clientSecret` สำหรับแอพลิเคชัน Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="8eec8-279">การดึงข้อมูลโทเค็น Azure Active Directory (`aadToken`) โดยการส่งการร้องขอ HTTP มีคุณสมบัติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8eec8-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="8eec8-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="8eec8-281">**วิธีการ** - `GET`</span><span class="sxs-lookup"><span data-stu-id="8eec8-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="8eec8-282">**ตัวเนื้อหา (ข้อมูลแบบฟอร์ม)**:</span><span class="sxs-lookup"><span data-stu-id="8eec8-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="8eec8-283">คีย์</span><span class="sxs-lookup"><span data-stu-id="8eec8-283">key</span></span> | <span data-ttu-id="8eec8-284">ค่า</span><span class="sxs-lookup"><span data-stu-id="8eec8-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="8eec8-285">รหัส_ไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="8eec8-285">client_id</span></span> | <span data-ttu-id="8eec8-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="8eec8-286">${aadAppId}</span></span> |
        | <span data-ttu-id="8eec8-287">ข้อมูลลับ_ไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="8eec8-287">client_secret</span></span> | <span data-ttu-id="8eec8-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="8eec8-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="8eec8-289">ชนิด_การให้สิทธิ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-289">grant_type</span></span> | <span data-ttu-id="8eec8-290">ข้อมูลประจำตัว_ไคลเอ็นต์</span><span class="sxs-lookup"><span data-stu-id="8eec8-290">client_credentials</span></span> |
        | <span data-ttu-id="8eec8-291">ทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="8eec8-291">resource</span></span> | <span data-ttu-id="8eec8-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="8eec8-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="8eec8-293">คุณควรได้รับ `aadToken` ในการตอบสนอง ซึ่งคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="8eec8-294">สร้างการร้องขอ JSON ที่คล้ายกับสิ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-294">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="8eec8-295">ที่ใด:</span><span class="sxs-lookup"><span data-stu-id="8eec8-295">Where:</span></span>
    - <span data-ttu-id="8eec8-296">ค่า `client_assertion` ต้องเป็น `aadToken` ที่คุณได้รับในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="8eec8-297">ค่า `context` ต้องเป็นรหัสสภาพแวดล้อมที่คุณต้องการปรับใช้ Add-in</span><span class="sxs-lookup"><span data-stu-id="8eec8-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="8eec8-298">ตั้งค่าอื่นๆ ทั้งหมด ตามที่แสดงในตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="8eec8-299">ส่งการร้องขอ HTTP ที่มีคุณสมบัติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8eec8-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="8eec8-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="8eec8-301">**วิธีการ** - `POST`</span><span class="sxs-lookup"><span data-stu-id="8eec8-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="8eec8-302">**ส่วนหัว HTTP** - รวมถึงเวอร์ชันของ API (คีย์คือ `Api-Version` และค่าเป็น `1.0`)</span><span class="sxs-lookup"><span data-stu-id="8eec8-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="8eec8-303">**ตัวเนื้อหา** - รวมถึงการร้องขอ JSON ที่คุณสร้างในขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="8eec8-304">คุณจะได้รับ `access_token` ในการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="8eec8-305">นี่คือสิ่งที่คุณต้องการในฐานะโทเคนผู้ถือสิทธิ์เพื่อเรียก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="8eec8-306">นี่คือตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="8eec8-307">คำขอตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-307">Sample Request</span></span>

<span data-ttu-id="8eec8-308">ในการอ้างอิงของคุณ ต่อไปนี้เป็นคำขอ http ตัวอย่าง คุณสามารถใช้เครื่องมือหรือภาษาการเขียนโค้ดใด ๆ เพื่อส่งคำขอนี้ เช่น ``Postman``</span><span class="sxs-lookup"><span data-stu-id="8eec8-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="8eec8-309">ตั้งค่าคอนฟิก API ความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="8eec8-310">ก่อนที่จะใช้บริการ คุณต้องทำการตั้งค่าคอนฟิกที่อธิบายไว้ในส่วนย่อยต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="8eec8-311">การตั้งค่าคอนฟิกอาจแตกต่างกันไปตามรายละเอียดของสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="8eec8-312">ส่วนใหญ่แล้วประกอบด้วยสี่ส่วน:</span><span class="sxs-lookup"><span data-stu-id="8eec8-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="8eec8-313">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="8eec8-314">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="8eec8-315">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="8eec8-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="8eec8-316">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="8eec8-317">การแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-317">Partitioning</span></span>

<span data-ttu-id="8eec8-318">การแบ่งพาร์ติชันสามารถมีผลกระทบต่อประสิทธิภาพการทำงานของ API ความสามารถในการมองเห็นสินค้าคงคลังได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="8eec8-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="8eec8-319">ขอแนะนำให้คุณกำหนดโครงร่างที่อนุญาตให้มีการจัดกลุ่มข้อมูลเล็กๆ ในขณะที่ยังคงอนุญาตให้มีการสอบถามข้อมูลที่มีความหมาย</span><span class="sxs-lookup"><span data-stu-id="8eec8-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="8eec8-320">`organizationId` (`dataAreaId` ใน Supply Chain Management) จะเป็นส่วนหนึ่งของการแบ่งพาร์ติชันเสมอ และตามค่าเริ่มต้น ความสามารถในการมองเห็นสินค้าคงคลังจะถูกตั้งค่าเป็นพาร์ติชันตามมิติเป็น *ไซต์ + สถานที่*</span><span class="sxs-lookup"><span data-stu-id="8eec8-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="8eec8-321">นี่หมายความว่าบริการต้องมีการสอบถามเสมอด้วยมิติเหล่านี้ที่กำหนดไว้ในตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="8eec8-322">*ไซต์* และ *สถานที่* เป็นมิติเริ่มต้นทั่วไปสองมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="8eec8-323">ใน Supply Chain Management มิติเหล่านี้เรียกว่า *ไซต์* (`InventSiteId`) และ *คลังสินค้า* (`InventLocationId`)</span><span class="sxs-lookup"><span data-stu-id="8eec8-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="8eec8-324">การตั้งค่าคอนฟิกมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-324">Dimension configurations</span></span>

<span data-ttu-id="8eec8-325">ความสามารถในการมองเห็นสินค้าคงคลังจะแสดงรายการของมิติเริ่มต้นทั่วไป เพื่อเปิดใช้งานการรวมระบบแหล่งที่มาหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="8eec8-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="8eec8-326">ตารางต่อไปนี้แสดงรายการมิติสินค้าคงคลังที่จะเป็นชื่อมิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="8eec8-327">ชนิดมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-327">Dimension type</span></span> | <span data-ttu-id="8eec8-328">ชื่อมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="8eec8-329">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="8eec8-330">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="8eec8-331">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="8eec8-332">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="8eec8-333">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="8eec8-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="8eec8-334">การติดตาม</span><span class="sxs-lookup"><span data-stu-id="8eec8-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="8eec8-335">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8eec8-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="8eec8-336">ที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="8eec8-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="8eec8-337">สถานะของสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="8eec8-338">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8eec8-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="8eec8-339">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8eec8-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="8eec8-340">คลังสินค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8eec8-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="8eec8-341">ชนิดของมิติที่แสดงรายการอยู่ในตารางก่อนหน้านี้ใช้สำหรับการอ้างอิงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="8eec8-342">คุณไม่จำเป็นต้องกำหนดชนิดมิติในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="8eec8-343">ถ้ามีมิติที่กำหนดเองอยู่และจำเป็นต้องโฟลว์ไปยังค่าเริ่มต้น เมื่อมีการใช้งานโดยความสามารถในการมองเห็นสินค้าคงคลัง คุณสามารถตั้งค่าคอนฟิก **ชื่อมิติที่กำหนดเอง** ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="8eec8-344">ระบบภายนอกเข้าถึงความสามารถในการมองเห็นสินค้าคงคลังผ่าน RESTful APIs ที่เปิดใช้งานข้อมูลปริมาณคงคลังคงเหลือในชุดที่กำหนดของมิติที่จะมีการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8eec8-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="8eec8-345">สำหรับการรวม ความสามารถในการมองเห็นสินค้าคงคลังจะช่วยให้คุณสามารถตั้งค่าคอนฟิก *แหล่งข้อมูลช่องทางภายนอก* และมิติแหล่งที่มาเป็น *มิติเป้าหมาย* ในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="8eec8-346">มิติเป้าหมายควรเป็นหนึ่งในรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="8eec8-347">มิติเริ่มต้นในความสามารถในการมองเห็นสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="8eec8-348">มิติที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-348">Custom dimensions</span></span>

<span data-ttu-id="8eec8-349">วัตถุประสงค์ของการตั้งค่าคอนฟิกมิติคือ การกำหนดมาตรฐานการรวมหลายระบบสำหรับการสอบถามบนมิติและเหตุการณ์การโพสต์กับมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="8eec8-350">การจัดทำดัชนี</span><span class="sxs-lookup"><span data-stu-id="8eec8-350">Indexing</span></span>

<span data-ttu-id="8eec8-351">ส่วนใหญ่การสอบถามปริมาณคงคลังคงเหลือไม่เพียงแค่อยู่ที่ระดับ "ยอดรวม" สูงสุด แต่คุณอาจต้องการดูผลลัพธ์ที่รวมโดยยึดตามมิติสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8eec8-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="8eec8-352">ความสามารถในการมองเห็นสินค้าคงคลังให้ความยืดหยุ่นโดยการอนุญาตให้คุณตั้งค่าดัชนี ซึ่งขึ้นอยู่กับมิติหรือชุดของมิติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="8eec8-353">ในขณะนี้ คุณสามารถตั้งค่าคอนฟิกดัชนีได้สูงสุดห้ารายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="8eec8-354">คุณต้องคำนึงถึงมิติหรือชุดของมิติที่คุณจะใช้ก่อนที่จะดำเนินการ เพื่อให้มั่นใจว่าจะตอบสนองความต้องการทางธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="8eec8-355">ตัวอย่างเช่น ถ้าคุณต้องการสอบถามผลิตภัณฑ์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="8eec8-356">สอบถามปริมาณคงคลังคงเหลือของผลิตภัณฑ์แบบรวมตามมิติ *สี* และ *ขนาด*</span><span class="sxs-lookup"><span data-stu-id="8eec8-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="8eec8-357">ในบางกรณี คุณต้องการสอบถามเกี่ยวกับผลิตภัณฑ์โดยรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="8eec8-358">คุณจะกำหนดดัชนีสองรายการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8eec8-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="8eec8-359">วงเล็บที่ว่างเปล่าจะรวมกันตามรหัสผลิตภัณฑ์ภายในการแบ่งพาร์ติชัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="8eec8-360">การจัดทำดัชนีจะกำหนดวิธีการที่คุณสามารถจัดกลุ่มผลลัพธ์ของคุณตามการตั้งค่าการสอบถาม `groupBy`</span><span class="sxs-lookup"><span data-stu-id="8eec8-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="8eec8-361">ในกรณีนี้ ถ้าคุณไม่ได้กำหนดค่า `groupBy` ใดๆ คุณจะได้รับผลรวมตาม `productid`</span><span class="sxs-lookup"><span data-stu-id="8eec8-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="8eec8-362">มิฉะนั้น ถ้าคุณกำหนด `groupBy` เป็น `groupBy=ColorId&groupBy=SizeId` คุณจะได้รับบรรทัดหลายบรรทัดที่ส่งคืน โดยยึดตามชุดสีและขนาดต่างๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="8eec8-363">คุณสามารถกำหนดเกณฑ์การสอบถามของคุณในเนื้อหาของคำขอ</span><span class="sxs-lookup"><span data-stu-id="8eec8-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="8eec8-364">ต่อไปนี้เป็นการสอบถามตัวอย่างเกี่ยวกับผลิตภัณฑ์ที่มีชุดสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="8eec8-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
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

<span data-ttu-id="8eec8-365">ปัจจุบัน ฟิลด์ `filters` เฉพาะ `ProductId` สนับสนุนค่าหลายค่าเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="8eec8-366">ถ้า `ProductId` เป็นแถวลำดับที่ว่างเปล่า ผลิตภัณฑ์ทั้งหมดจะถูกสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8eec8-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="8eec8-367">การวัดแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-367">Custom measurement</span></span>

<span data-ttu-id="8eec8-368">ปริมาณการประเมินเริ่มต้นจะเชื่อมโยงกับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8eec8-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="8eec8-369">อย่างไรก็ตาม คุณอาจต้องการมีปริมาณที่รวมกันของชุดการประเมินเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="8eec8-370">เมื่อต้องการดำเนินการนี้ คุณสามารถมีการตั้งค่าคอนฟิกของปริมาณที่กำหนดเอง ซึ่งจะถูกเพิ่มเข้าไปในผลลัพธ์ของการสอบถามปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8eec8-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="8eec8-371">ฟังก์ชันนี้จะช่วยให้คุณสามารถกำหนดชุดของการวัดที่จะเพิ่ม และ/หรือชุดของการวัดที่จะถูกลบ เพื่อสร้างการวัดที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8eec8-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="8eec8-372">ตัวอย่างเช่น ด้วยเงื่อนไขการสอบถามต่อไปนี้ คุณจะตั้งค่าคอนฟิกปริมาณการวัดแบบกำหนดเองเป็น `MyCustomAvailableforReservation` ที่จะใช้โดยระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="8eec8-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="8eec8-373">ระบบปริมาณการใช้วัสดุ</span><span class="sxs-lookup"><span data-stu-id="8eec8-373">Consumption system</span></span> | <span data-ttu-id="8eec8-374">ผู้วัดที่มีการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-374">Calculated measurers</span></span> | <span data-ttu-id="8eec8-375">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8eec8-375">Data source</span></span> | <span data-ttu-id="8eec8-376">ตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8eec8-376">Modifier</span></span> | <span data-ttu-id="8eec8-377">ชนิดการคำนวณของตัวแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8eec8-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="8eec8-378">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="8eec8-379">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="8eec8-380">การลบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="8eec8-381">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="8eec8-382">การลบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="8eec8-383">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="8eec8-384">การเพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="8eec8-385">การลบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="8eec8-386">การลบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-386">Subtraction</span></span> |

<span data-ttu-id="8eec8-387">การสอบถามในปริมาณการวัดที่กำหนดเองจะส่งคืนผลลัพธ์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="8eec8-388">ผลลัพธ์ `MyCustomAvailableforReservation` จะขึ้นอยู่กับการตั้งค่าการคำนวณในการวัดที่กำหนดเองเป็น:</span><span class="sxs-lookup"><span data-stu-id="8eec8-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="8eec8-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="8eec8-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="8eec8-390">การโพสต์การเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8eec8-390">Posting on-hand changes</span></span>

<span data-ttu-id="8eec8-391">URL ที่แน่นอนซึ่งจะมีการโพสต์เหตุการณ์ จะขึ้นอยู่กับภูมิภาคทางภูมิศาสตร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="8eec8-392">ซึ่งจะใช้ฟอร์ม:</span><span class="sxs-lookup"><span data-stu-id="8eec8-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="8eec8-393">เมื่อมีการพิสูจน์ตัวจริง สามารถใช้ URL นี้พร้อมกับวิธีการ HTTP `POST` เพื่อส่งเหตุการณ์ของการเปลี่ยนแปลงปริมาณคงคลังคงเหลือไปยังบริการ</span><span class="sxs-lookup"><span data-stu-id="8eec8-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="8eec8-394">ส่วนหัวพิเศษจะถูกใช้สำหรับการสื่อสารกับบริการ Dynamics 365 ผ่านคำขอ HTTP ซึ่งแสดงรหัสสภาพแวดล้อมของอินสแตนซ์ Supply Chain Management ที่ข้อมูลถูกลิงค์ไปถึง</span><span class="sxs-lookup"><span data-stu-id="8eec8-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="8eec8-395">ตัวอย่างเช่น:</span><span class="sxs-lookup"><span data-stu-id="8eec8-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="8eec8-396">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 1</span><span class="sxs-lookup"><span data-stu-id="8eec8-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="8eec8-397">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณจะตั้งค่าการตั้งค่าคอนฟิกมิติใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="8eec8-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8eec8-398">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8eec8-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8eec8-399">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8eec8-400">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="8eec8-401">การโพสต์ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือ 2</span><span class="sxs-lookup"><span data-stu-id="8eec8-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="8eec8-402">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8eec8-403">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="8eec8-404">คุณสมบัติฟิลด์ของเอกสาร JSON</span><span class="sxs-lookup"><span data-stu-id="8eec8-404">JSON document field properties</span></span>

<span data-ttu-id="8eec8-405">ฟิลด์จากตัวอย่างการสอบถาม JSON ที่ให้ไว้ก่อนหน้านี้ มีคุณสมบัติที่แสดงรายการอยู่ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="8eec8-406">ฟิลด์ ID</span><span class="sxs-lookup"><span data-stu-id="8eec8-406">Field ID</span></span> | <span data-ttu-id="8eec8-407">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8eec8-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="8eec8-408">รหัสเฉพาะสำหรับเหตุการณ์การเปลี่ยนแปลงเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8eec8-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="8eec8-409">รหัสนี้จะใช้เพื่อให้แน่ใจว่า ถ้าการสื่อสารกับบริการล้มเหลวในระหว่างการโพสต์ การส่งเหตุการณ์อีกครั้งจะไม่มีผลในเหตุการณ์เดียวกันที่ถูกนับสองครั้งในระบบ</span><span class="sxs-lookup"><span data-stu-id="8eec8-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="8eec8-410">ตัวระบุขององค์กรที่ลิงก์ไปยังเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="8eec8-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="8eec8-411">นี่จะแม็ปไปยังองค์กร Supply Chain Management หรือรหัสพื้นที่ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8eec8-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="8eec8-412">ตัวระบุของผลิตภัณฑ์ที่สงสัย</span><span class="sxs-lookup"><span data-stu-id="8eec8-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="8eec8-413">ปริมาณที่ต้องมีการเปลี่ยนแปลงปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="8eec8-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="8eec8-414">ตัวอย่างเช่น ถ้าตัวอย่างเช่น เบเกิลใหม่ 10 ชิ้นถูกเพิ่มไปยังชั้นวาง ค่านี้จะเป็น 10</span><span class="sxs-lookup"><span data-stu-id="8eec8-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="8eec8-415">ถ้าเบเกิล 3 ชิ้นถูกเอาออกจากชั้นวางหรือขายแล้ว ค่านี้จะเป็น -3</span><span class="sxs-lookup"><span data-stu-id="8eec8-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="8eec8-416">แหล่งข้อมูลของมิติที่ใช้ในการโพสต์เหตุการณ์การเปลี่ยนแปลงและการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8eec8-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="8eec8-417">ถ้าคุณระบุแหล่งข้อมูล คุณสามารถใช้มิติที่กำหนดเองจากแหล่งข้อมูลที่ระบุได้</span><span class="sxs-lookup"><span data-stu-id="8eec8-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="8eec8-418">ด้วยการตั้งค่าคอนฟิกมิติ ความสามารถในการมองเห็นสินค้าคงคลังสามารถแม็ปมิติที่กำหนดเองกับมิติเริ่มต้นทั่วไป</span><span class="sxs-lookup"><span data-stu-id="8eec8-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="8eec8-419">ถ้าไม่มีการระบุ `dimensionDataSource` คุณสามารถใช้มิติเริ่มต้นทั่วไปในการสอบถามของคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="8eec8-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="8eec8-420">ถุงแบบไดนามิกของคู่คีย์/ค่า</span><span class="sxs-lookup"><span data-stu-id="8eec8-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="8eec8-421">การทำเช่นนี้จะแม็ปกับบางมิติใน Supply Chain Management แต่คุณยังสามารถเพิ่มมิติที่กำหนดเองได้ด้วย (เช่น *แหล่งที่มา*) ซึ่งอาจแสดงว่าเหตุการณ์นี้มาจาก Supply Chain Management หรือระบบภายนอก</span><span class="sxs-lookup"><span data-stu-id="8eec8-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="8eec8-422">การสอบถามปริมาณคงคลังคงเหลือปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-422">Querying current on-hand</span></span>

<span data-ttu-id="8eec8-423">ปลายทางสำหรับการสอบถามปริมาณคงคลังคงเหลือปัจจุบันจะมี URL ที่คล้ายกัน:</span><span class="sxs-lookup"><span data-stu-id="8eec8-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="8eec8-424">ซึ่งจะมีการสอบถามด้วยวิธีการ HTTP `POST`</span><span class="sxs-lookup"><span data-stu-id="8eec8-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="8eec8-425">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 1</span><span class="sxs-lookup"><span data-stu-id="8eec8-425">Current on-hand query example 1</span></span>

<span data-ttu-id="8eec8-426">ตัวอย่างนี้แสดงสถานการณ์จำลองที่คุณดำเนินการการตั้งค่าคอนฟิกมิติเสร็จสมบูรณ์แล้วใน Power Apps</span><span class="sxs-lookup"><span data-stu-id="8eec8-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8eec8-427">ใช้การสอบถามต่อไปนี้เพื่อตั้งค่าคอนฟิกการแม็ปมิติใน Power Apps:</span><span class="sxs-lookup"><span data-stu-id="8eec8-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8eec8-428">ขณะนี้คุณสามารถระบุ `dimensionDataSource` และใช้มิติที่กำหนดเองในการสอบถามของคุณ</span><span class="sxs-lookup"><span data-stu-id="8eec8-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8eec8-429">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="8eec8-430">คุณสามารถระบุ `DimensionDataSource` ใน `filters` และระบุมิติที่กำหนดเองในทั้ง `filters` และ `groupByValues`</span><span class="sxs-lookup"><span data-stu-id="8eec8-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="8eec8-431">ระบบจะแปลงมิติที่กำหนดเองเป็นมิติพื้นฐานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8eec8-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="8eec8-432">ตัวอย่างการสอบถามปริมาณคงคลังคงเหลือปัจจุบัน 2</span><span class="sxs-lookup"><span data-stu-id="8eec8-432">Current on-hand query example 2</span></span>

<span data-ttu-id="8eec8-433">ตัวอย่างนี้แสดงสถานการณ์จำลองที่ไม่มีการตั้งค่าการแม็ปสำหรับการตั้งค่าคอนฟิกมิติใน Power Apps ดังนั้นการโพสต์ยังควรใช้มิติพื้นฐานด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="8eec8-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8eec8-434">มิติทั้งหมดต้องเป็นมิติฐาน เมื่อฟิลด์ `dimensionDataSource` ภายใต้ `filters` เป็น null ว่างเปล่า หรือช่องว่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="8eec8-435">ผลลัพธ์การส่งคืนตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8eec8-435">Example return result</span></span>

<span data-ttu-id="8eec8-436">การสอบถามที่แสดงในตัวอย่างก่อนหน้านี้ อาจส่งผลให้เกิดผลลัพธ์ดังนี้</span><span class="sxs-lookup"><span data-stu-id="8eec8-436">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="8eec8-437">โปรดสังเกตว่าฟิลด์ปริมาณมีการจัดโครงสร้างเป็นพจนานุกรมของการวัดและค่าที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8eec8-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
