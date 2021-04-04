---
title: ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด
description: หัวข้อนี้แสดงภาพรวมของโซลูชันของผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Sales
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70ea2638408296df283a030dedce03b22cb57d81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248750"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="4f784-103">ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด</span><span class="sxs-lookup"><span data-stu-id="4f784-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f784-104">โซลูชั่นผู้ที่มีแนวโน้มจะเป็นลูกค้าเเงินสดให้การซิงโครไนส์โดยตรงระหว่าง Dynamics 365 Supply Chain Management และ Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="4f784-105">เท็มเพลตผู้ผู้ที่มีแนวโน้มจะเป็นลูกค้าเเงินสดที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลจะเปิดใช้งานโฟลว์ของข้อมูลสำหรับบัญชี ผู้ติดต่อ ผลิตภัณฑ์ ใบเสนอราคาขาย ใบสั่งขาย และใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="4f784-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="4f784-106">ในขณะที่มีการถ่ายโอนข้อมูล คุณสามารถดำเนินกิจกรรมส่งเสริมการขายและการตลาดใน Sales และคุณสามารถแฮนเดิลการเติมเต็มสินค้าตามใบสั่งโดยใช้การจัดการสินค้าคงคลังใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="4f784-107">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด ให้ดูวิดีโอ YouTube แบบย่อ [การรวมผู้ที่มีแนวโน้มจะเป็นลูกค้ากับเงินสด](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span><span class="sxs-lookup"><span data-stu-id="4f784-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="4f784-108">ในเวอร์ชันปัจจุบัน โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดแสดงชนิดของการซิงโครไนส์โดยตรงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f784-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="4f784-109">ซิงโครไนส์บัญชีโดยตรงจาก Sales ไปยังรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-109">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="4f784-110">ซิงโครไนส์ผลิตภัณฑ์โดยตรงจาก Supply Chain Management ไปยังผลิตภัณฑ์ใน Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-110">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="4f784-111">ซิงโครไนส์ผู้ติดต่อโดยตรงจาก Sales ไปยังผู้ติดต่อหรือรายชื่อลูกค้าใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-111">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="4f784-112">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Sales ไปยัง Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-112">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="4f784-113">การซิงโครไนส์ใบสั่งขายโดยตรงระหว่าง Sales และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-113">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="4f784-114">ซิงโครไนส์ส่วนหัวและรายการของใบเสนอราคาขายโดยตรงจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-114">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="4f784-115">ระบบต้องใช้กับ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4f784-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="4f784-116">การรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดได้รับการสนับสนุนในรุ่นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f784-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="4f784-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (ธันวาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="4f784-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="4f784-118">Dynamics 365 for Finance and Operations, Enterprise Edition (ธันวาคม 2017) - รุ่นของแอพลิเคชัน 7.3.11971.56116 กับการอัพเดแพลตฟอร์ม 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="4f784-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="4f784-119">Dynamics 365 for Finance and Operations, Enterprise Edition (กรกฎาคม 2017)</span><span class="sxs-lookup"><span data-stu-id="4f784-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="4f784-120">Dynamics 365 for Finance and Operations, Enterprise Edition (กรกฎาคม 2017) - ที่มีการอัพเดตแพลตฟอร์ม 8 (รุ่นของแอพลิเคชัน 7.2.11792.56024 ที่มีบิลด์ของแพลตฟอร์ม 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="4f784-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="4f784-121">จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f784-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="4f784-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Sales ไปยัง Supply Chain Management ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f784-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="4f784-123">ยังมีการปรับปรุงอื่นๆ อีกหลายส่วน</span><span class="sxs-lookup"><span data-stu-id="4f784-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="4f784-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Supply Chain Management ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f784-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="4f784-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – โปรแกรมแก้ไขด่วนนี้ทำให้สามารถซิงโครไนส์ใบสั่งขายจาก Supply Chain Management ไปยัง Sales ผ่านทางคุณลักษณะการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f784-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4f784-126">คุณเพียงต้องติดตั้ง KB4045570 เนื่องจากการติดตั้งรวมการเปลี่ยนแปลงจากของโปรแกรมแก้ไขด่วนอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4f784-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="4f784-127">Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016)</span><span class="sxs-lookup"><span data-stu-id="4f784-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="4f784-128">Dynamics 365 for Finance and Operations รุ่น 1611 (พฤศจิกายน 2016) ที่มีการอัพเดตแพลตฟอร์ม 8 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="4f784-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="4f784-129">จำเป็นต้องมีโปรแกรมแก้ไขด่วนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f784-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="4f784-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - เปิดใช้งานการซิงโครไนส์ใบสั่งขายกับตัวรวมข้อมูลจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="4f784-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - เปิดใช้งานการซิงโครไนส์ส่วนหัวและรายการกับตัวรวมข้อมูลจาก Supply Chain Management ไปยัง Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="4f784-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - จำเป็นต้องมีการสนับสนุนสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดผ่านทางเอนทิตีข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f784-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="4f784-133">หลังจากที่คุณติดตั้งโปรแกรมแก้ไขด่วน คุณต้องทริกเกอร์ชุดงานต่อไปนี้จากแบบฟอร์ม **SalesPopulateProspectToCash**</span><span class="sxs-lookup"><span data-stu-id="4f784-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="4f784-134">แบบฟอร์มนี้ถูกซ่อนไว้ เนื่องจากคุณต้องการเพียงครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="4f784-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="4f784-135">เพื่อเข้าถึงแบบฟอร์ม ให้ล็อกอินเข้าสู่สภาพแวดล้อม และเพิ่มรายการต่อไปนี้ไปยัง URL ในที่อยู่เบราเซอร์ของคุณ: *&mi=action:SalesPopulateProspectToCash* ตัวอย่างเช่น `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`</span><span class="sxs-lookup"><span data-stu-id="4f784-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="4f784-136">เมื่อแบบฟอร์มเปิดขึ้น คลิกตกลง</span><span class="sxs-lookup"><span data-stu-id="4f784-136">When the form opens, click OK.</span></span> <span data-ttu-id="4f784-137">การดำเนินการนี้จะเติมข้อมูลในฟิลด์ **LineCreationSequnceNumber** ใหม่ ในตาราง **SalesLine** **SalesQuotationLine** และ **CustInvoiceTrans** ด้วยค่าที่ไม่ซ้ำกัน และรีเฟรชรายการผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4f784-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="4f784-138">นี่เป็นสิ่งจำเป็นสำหรับการรวมผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสดกับการทำงาน</span><span class="sxs-lookup"><span data-stu-id="4f784-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="4f784-139">ความต้องการของระบบสำหรับ Sales</span><span class="sxs-lookup"><span data-stu-id="4f784-139">System requirements for Sales</span></span>

<span data-ttu-id="4f784-140">เมื่อต้องการใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f784-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="4f784-141">Dynamics 365 Sales รุ่น 1612 (8.2.1.207) (DB 8.2.1.207) ออนไลน์หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4f784-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="4f784-142">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเงินสดสำหรับ Dynamics 365 Sales รุ่น 1.15.0.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="4f784-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="4f784-143">โซลูชันนี้มีให้การดาวน์โหลดจาก AppSource</span><span class="sxs-lookup"><span data-stu-id="4f784-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="4f784-144">[ดาวน์โหลด Dynamics 365 ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)</span><span class="sxs-lookup"><span data-stu-id="4f784-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]