---
title: "ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด"
description: "หัวข้อนี้แสดงภาพรวมของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดระหว่าง Microsoft Dynamics 365 for Finance and Operations, Enterprise edition และ Microsoft Dynamics 365 for Sales"
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: th-th
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e1f42-103">ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="e1f42-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1f42-104">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดให้การซิงโครไนส์โดยตรงระหว่าง Dynamics 365 for Finance and Operations, Enterprise edition และ Microsoft Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="e1f42-105">เท็มเพลตผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล จะเปิดใช้งานโฟลว์ของข้อมูลสำหรับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขายระหว่าง Finance and Operations และ Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="e1f42-106">ขณะที่มีการถ่ายโอนข้อมูลระหว่าง Finance and Operations และ Sales คุณสามารถดำเนินกิจกรรมการขายและการตลาดใน Sales และคุณสามารถจัดการการเติมสินค้าตามใบสั่งโดยใช้การบริหารสินค้าคงคลัง Finance and Operations ได้</span><span class="sxs-lookup"><span data-stu-id="e1f42-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="e1f42-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ดูวิดีโอ YouTube แบบย่อ:</span><span class="sxs-lookup"><span data-stu-id="e1f42-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="e1f42-108">ในเวอร์ชันปัจจุบัน โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดแสดงชนิดของการซิงโครไนส์โดยตรงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1f42-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="e1f42-109">รักษาบัญชีใน Sales และซิงโครไนส์โดยตรงจาก Sales ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1f42-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="e1f42-110">รักษาผลิตภัณฑ์ใน Finance and Operations และซิงโครไนส์โดยตรงไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="e1f42-111">รักษาผู้ติดต่อใน Sales และซิงโครไนส์โดยตรงไปยังผู้ติดต่อหรือลูกค้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1f42-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="e1f42-112">ซิงโครไนส์ใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Finance and Operations (เท็มเพลตที่ค้างอยู่รอการนำออกใช้)</span><span class="sxs-lookup"><span data-stu-id="e1f42-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="e1f42-113">ซิงโครไนส์ใบสั่งขายโดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="e1f42-114">ซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Finance and Operations (เท็มเพลตที่ค้างอยู่รอการนำออกใช้)</span><span class="sxs-lookup"><span data-stu-id="e1f42-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="e1f42-115">ซิงโครไนส์ใบแจ้งหนี้โดยตรงจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="e1f42-116">ความต้องการของระบบสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1f42-116">System requirements for Finance and Operations</span></span>

<span data-ttu-id="e1f42-117">การรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้รับการสนับสนุนในรุ่นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1f42-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="e1f42-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (ธันวาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="e1f42-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="e1f42-119">Dynamics 365 for Finance and Operations, Enterprise edition (ธันวาคม 2017) - การสร้างแอพลิเคชัน 7.3.11971.56116 พร้อมกับการอัพเดตแพลตฟอร์ม 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="e1f42-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="e1f42-120">Dynamics 365 for Finance and Operations, Enterprise Edition (กรกฎาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="e1f42-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="e1f42-121">Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) - พร้อมกับการอัพเดตแพลตฟอร์ม 8 (การสร้างแอพลิเคชัน 7.2.11792.56024 พร้อมกับการสร้างแพลตฟอร์ม 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="e1f42-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="e1f42-122">จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1f42-122">The following hotfixes are required:</span></span>

    - <span data-ttu-id="e1f42-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Sales ไปยัง Finance and Operations ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e1f42-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="e1f42-124">ยังมีการปรับปรุงอื่นๆ อีกหลายส่วน</span><span class="sxs-lookup"><span data-stu-id="e1f42-124">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="e1f42-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์รายการใบสั่งขายจาก Finance and Operations ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e1f42-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="e1f42-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Finance and Operations ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e1f42-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e1f42-127">คุณเพียงต้องติดตั้ง KB4045570 เนื่องจากการติดตั้งรวมการเปลี่ยนแปลงจากของโปรแกรมแก้ไขด่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="e1f42-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="e1f42-128">Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="e1f42-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="e1f42-129">Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016) ที่มีการอัพเดตแพลตฟอร์ม 8 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="e1f42-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="e1f42-130">จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1f42-130">The following hotfixes are required:</span></span>

    - <span data-ttu-id="e1f42-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - เปิดใช้งานการซิงโครไนส์ใบสั่งขายกับตัวรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="e1f42-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - เปิดใช้งานการซิงโครไนส์ส่วนหัวและรายการของใบสั่งขายกับตัวรวมข้อมูลจาก Finance and Operations ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="e1f42-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - จำเป็นต้องมีการสนับสนุนสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดผ่านทางเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e1f42-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e1f42-134">หลังจากที่คุณติดตั้งโปรแกรมแก้ไขด่วน คุณต้องทริกเกอร์ชุดงานต่อไปนี้จากแบบฟอร์ม **SalesPopulateProspectToCash**</span><span class="sxs-lookup"><span data-stu-id="e1f42-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="e1f42-135">แบบฟอร์มนี้ถูกซ่อนไว้ เนื่องจากคุณต้องการเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="e1f42-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="e1f42-136">เพื่อเข้าถึงแบบฟอร์ม ให้ล็อกอินเข้าสู่สภาพแวดล้อม และเพิ่มรายการต่อไปนี้ไปยัง URL ในที่อยู่เบราเซอร์ของคุณ: &mi=action:SalesPopulateProspectToCash ตัวอย่างเช่น `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`</span><span class="sxs-lookup"><span data-stu-id="e1f42-136">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="e1f42-137">เมื่อแบบฟอร์มเปิดขึ้น คลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="e1f42-137">When the form opens, click OK.</span></span> <span data-ttu-id="e1f42-138">การดำเนินการนี้จะเติมข้อมูลในฟิลด์ **LineCreationSequnceNumber** ใหม่ ในตาราง **SalesLine** **SalesQuotationLine** และ **CustInvoiceTrans** ด้วยค่าที่ไม่ซ้ำกัน และรีเฟรชรายการผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e1f42-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="e1f42-139">นี่เป็นสิ่งจำเป็นสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดกับการทำงาน</span><span class="sxs-lookup"><span data-stu-id="e1f42-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="e1f42-140">ความต้องการของระบบสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-140">System requirements for Sales</span></span>

<span data-ttu-id="e1f42-141">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e1f42-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="e1f42-142">Dynamics 365 for Sales รุ่น 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e1f42-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="e1f42-143">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales รุ่น 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="e1f42-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e1f42-144">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="e1f42-144">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="e1f42-145">ดาวน์โหลด [ไฟล์ Zip ของแพคเกจโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดสำหรับ Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) จาก CustomerSource</span><span class="sxs-lookup"><span data-stu-id="e1f42-145">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="e1f42-146">ต้องแน่ใจว่าไฟล์ Zip ไม่ถูกบล็อค</span><span class="sxs-lookup"><span data-stu-id="e1f42-146">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="e1f42-147">มิฉะนั้น เมื่อคุณพยายามติดตั้งแพคเกจโซลูชัน คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ "ไม่พบแพคเกจนำเข้า"</span><span class="sxs-lookup"><span data-stu-id="e1f42-147">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="e1f42-148">เพื่อยกเลิกการบล็อคไฟล์ Zip คลิกขวา แล้วเลือก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="e1f42-148">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="e1f42-149">เลือก **ยกเลิกการบล็อก**</span><span class="sxs-lookup"><span data-stu-id="e1f42-149">Select **Unblock**.</span></span>
3. <span data-ttu-id="e1f42-150">Unzip และรัน **PackageDeployer.exe**</span><span class="sxs-lookup"><span data-stu-id="e1f42-150">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="e1f42-151">ติดตั้งโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดบนอินสแตนซ์ Sales ของคุณ</span><span class="sxs-lookup"><span data-stu-id="e1f42-151">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="e1f42-152">เลือก **Office 365** เป็นชนิดการปรับใช้</span><span class="sxs-lookup"><span data-stu-id="e1f42-152">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="e1f42-153">เลือก **แสดงขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="e1f42-153">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="e1f42-154">สำหรับการติดตั้งด่วน เลือกภูมิภาค</span><span class="sxs-lookup"><span data-stu-id="e1f42-154">For a quick installation, select a region.</span></span> <span data-ttu-id="e1f42-155">ถ้าคุณเลือก **ไม่ทราบ** ระบบจะค้นหาทุกภูมิภาค และจะใช้เวลานานมากขึ้นในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="e1f42-155">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="e1f42-156">ป้อนชื่อผู้ใช้และรหัสผ่านของผู้ใช้ที่เป็นผู้ดูแลระบบที่มีสิทธิ์ในการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="e1f42-156">Enter the user name and password of an admin user who has installation rights.</span></span>



