---
title: "ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด"
description: "หัวข้อแสดงภาพรวมของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดระหว่าง Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: th-th
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="4b45b-103">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="4b45b-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4b45b-104">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดใช้ [การรวมข้อมูล](/common-data-service/entity-reference/dynamics-365-integration) ในการซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Dynamics 365 for Sales ผ่าน Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="4b45b-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="4b45b-105">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลจะเปิดใช้งานขั้นตอนของข้อมูลบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="4b45b-106">ขณะที่มีการถ่ายโอนข้อมูลระหว่าง Finance and Operations และ Sales คุณสามารถดำเนินกิจกรรมการขายและการตลาดใน Dynamics 365 สำหรับการขาย และจัดการกระบวนการเติมสินค้าตามใบสั่งใน Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="4b45b-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="4b45b-107">โซลูชันนี้มีการรวมในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b45b-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="4b45b-108">รักษาบัญชีใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="4b45b-109">รักษาผู้ติดต่อใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="4b45b-110">รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="4b45b-111">สร้างใบเสนอราคาขายใน Sales และซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="4b45b-112">สร้างใบสั่งขายใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="4b45b-113">สร้างใบแจ้งหนี้การขายใน Finance and Operations และซิงโครไนส์กับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="4b45b-114">โซลูชันนี้มีการซิงโครไนส์โดยตรงในพื้นที่ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b45b-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="4b45b-115">รักษาบัญชีใน Sales และซิงโครไนส์โดยตรงจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="4b45b-116">รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์โดยตรงกับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="4b45b-117">รักษาผู้ติดต่อใน Sales และซิงโครไนส์โดยตรงไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="4b45b-118">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="4b45b-119">สร้างใบสั่งขายใน Finance and Operations และซิงโครไนส์โดยตรงกับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="4b45b-120">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="4b45b-121">ซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b45b-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="4b45b-122">สร้างใบแจ้งหนี้การขายใน Finance and Operations และซิงโครไนส์โดยตรงกับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="4b45b-123">ความต้องการของระบบสำหรับ Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="4b45b-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="4b45b-124">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b45b-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="4b45b-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) พร้อมกับการอัพเดตแพลตฟอร์ม 8 (แอพลิเคชัน 7.2.11792.56024 พร้อมกับแพลตฟอร์ม 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="4b45b-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="4b45b-126">โปรแกรมแก้ไขด่วนสำหรับ Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="4b45b-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="4b45b-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - โปรแกรมแก้ไขด่วนนี้เปิดใช้งานการสนับสนุนสำหรับการซิงโครไนส์ใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Sales ไปยัง Finance and Operations พร้อมด้วยหมายเลขของส่วนเพิ่มเติมอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4b45b-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="4b45b-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="4b45b-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) -โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์บรรทัดใบสั่งขายกับคุณลักษณะการรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="4b45b-130">**หมายเหตุ**: คุณเพียงต้องติดตั้ง KB4045570 เนื่องจากการติดตั้งรวมการเปลี่ยนแปลงจากของ KB อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4b45b-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="4b45b-131">ข้อกำหนดของระบบสำหรับ Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="4b45b-132">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b45b-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="4b45b-133">Dynamics 365 for Sales รุ่น 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="4b45b-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="4b45b-134">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales เวอร์ชัน 1.14.0.0 (v14) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4b45b-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4b45b-135">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="4b45b-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="4b45b-136">ดาวน์โหลด [ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับไฟล์ Zip ของแพคเกจโซลูชัน Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) ใน CustomerSource</span><span class="sxs-lookup"><span data-stu-id="4b45b-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="4b45b-137">ตรวจสอบว่าไฟล์ Zip ไม่ถูกบล็อคเพื่อที่คุณจะได้ไม่ได้รับข้อความแสดงข้อผิดพลาด "ไม่พบแพคเกจการนำเข้า" เมื่อคุณติดตั้งแพคเกจโซลูชัน</span><span class="sxs-lookup"><span data-stu-id="4b45b-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="4b45b-138">เมื่อต้องการยกเลิกการบล็อคไฟล์ ให้ทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4b45b-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="4b45b-139">คลิกขวาที่ไฟล์ Zip</span><span class="sxs-lookup"><span data-stu-id="4b45b-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="4b45b-140">เลือก **คุณสมบัติ** แล้วเลือก **ยกเลิกการบล็อค**</span><span class="sxs-lookup"><span data-stu-id="4b45b-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="4b45b-141">Unzip และรัน PackageDeployer.exe</span><span class="sxs-lookup"><span data-stu-id="4b45b-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="4b45b-142">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดในอินสแตนซ์ Sales ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4b45b-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="4b45b-143">เลือกชนิดการปรับใช้ **Office 365**</span><span class="sxs-lookup"><span data-stu-id="4b45b-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="4b45b-144">เลือก **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="4b45b-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="4b45b-145">สำหรับการติดตั้งด่วน เลือก **ภูมิภาค**</span><span class="sxs-lookup"><span data-stu-id="4b45b-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="4b45b-146">ถ้าคุณเลือก **ไม่ทราบ** ระบบจะค้นหาทุกภูมิภาค และจะใช้เวลานานในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="4b45b-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="4b45b-147">ป้อน **ชื่อผู้ใช้** และ **รหัสผ่าน** สำหรับผู้ดูแลที่มีสิทธิ์ของผู้ใช้ในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="4b45b-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

