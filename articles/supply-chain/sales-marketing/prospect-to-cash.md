---
title: "ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด"
description: "หัวข้อแสดงภาพรวมของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดระหว่าง Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="45bb7-103">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="45bb7-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="45bb7-104">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดใช้ [การรวมข้อมูล](/common-data-service/entity-reference/dynamics-365-integration) ในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales ผ่าน Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="45bb7-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="45bb7-105">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลจะเปิดใช้งานขั้นตอนของข้อมูลบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="45bb7-106">ขณะที่มีการถ่ายโอนข้อมูลระหว่าง Finance and Operations และ Sales คุณสามารถดำเนินกิจกรรมการขายและการตลาดใน Dynamics 365 สำหรับการขาย และจัดการกระบวนการเติมสินค้าตามใบสั่งใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="45bb7-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="45bb7-107">โซลูชันนี้มีการรวมในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45bb7-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="45bb7-108">รักษาบัญชีใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="45bb7-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="45bb7-109">รักษาผู้ติดต่อใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="45bb7-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="45bb7-110">รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="45bb7-111">สร้างใบเสนอราคาขายใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="45bb7-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="45bb7-112">สร้างใบสั่งขายใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="45bb7-113">สร้างใบแจ้งหนี้การขายใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="45bb7-114">ความต้องการของระบบสำหรับ Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="45bb7-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="45bb7-115">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45bb7-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="45bb7-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) พร้อมกับการอัพเดตแพลตฟอร์ม 8 (แอพลิเคชัน 7.2.11792.56024 พร้อมกับแพลตฟอร์ม 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="45bb7-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="45bb7-117">โปรแกรมแก้ไขด่วนสองรายการสำหรับ Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="45bb7-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="45bb7-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="45bb7-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="45bb7-120">**หมายเหตุ**: คุณเพียงต้องติดตั้ง KB4036524 เนื่องจากการติดตั้งมีการเปลี่ยนแปลงจาก KB4036461</span><span class="sxs-lookup"><span data-stu-id="45bb7-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="45bb7-121">ข้อกำหนดของระบบสำหรับ Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="45bb7-122">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45bb7-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="45bb7-123">Dynamics 365 for Sales เวอร์ชัน 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์ หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="45bb7-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="45bb7-124">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="45bb7-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="45bb7-125">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="45bb7-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="45bb7-126">ดาวน์โหลด [ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับไฟล์ Zip ของแพคเกจโซลูชัน Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) ใน CustomerSource</span><span class="sxs-lookup"><span data-stu-id="45bb7-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="45bb7-127">ตรวจสอบว่าไฟล์ Zip ไม่ถูกบล็อคเพื่อที่คุณจะได้ไม่ได้รับข้อความแสดงข้อผิดพลาด "ไม่พบแพคเกจการนำเข้า" เมื่อคุณติดตั้งแพคเกจโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="45bb7-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="45bb7-128">เมื่อต้องการยกเลิกการบล็อคไฟล์ ให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="45bb7-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="45bb7-129">คลิกขวาที่ไฟล์ Zip</span><span class="sxs-lookup"><span data-stu-id="45bb7-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="45bb7-130">เลือก **คุณสมบัติ** แล้วเลือก **ยกเลิกการบล็อค**</span><span class="sxs-lookup"><span data-stu-id="45bb7-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="45bb7-131">Unzip และรัน PackageDeployer.exe</span><span class="sxs-lookup"><span data-stu-id="45bb7-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="45bb7-132">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดในอินสแตนซ์ Sales ของคุณ</span><span class="sxs-lookup"><span data-stu-id="45bb7-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="45bb7-133">เลือกชนิดการปรับใช้ **Office 365**</span><span class="sxs-lookup"><span data-stu-id="45bb7-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="45bb7-134">เลือก **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="45bb7-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="45bb7-135">สำหรับการติดตั้งด่วน เลือก **ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="45bb7-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="45bb7-136">ถ้าคุณเลือก **ไม่ทราบ** ระบบจะค้นหาทุกภูมิภาค และจะใช้เวลานานในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="45bb7-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="45bb7-137">ป้อน **ชื่อผู้ใช้** และ **รหัสผ่าน** สำหรับผู้ดูแลที่มีสิทธิ์ของผู้ใช้ในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="45bb7-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

