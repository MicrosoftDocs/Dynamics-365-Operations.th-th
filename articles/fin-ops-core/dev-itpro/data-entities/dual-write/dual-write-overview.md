---
title: การรวมข้อมูลแบบใกล้เวลาจริงกับ Common Data Service
description: หัวข้อนี้แสดงภาพรวมของการรวมระหว่าง Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020042"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="90884-103">การรวมข้อมูลแบบใกล้เวลาจริงกับ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90884-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="90884-104">ในโลกดิจิทัลปัจจุบัน ระบบนิเวศธุรกิจใช้แอปพลิเคชัน Microsoft Dynamics 365 ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="90884-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="90884-105">เนื่องจากข้อมูลจากบุคคล ลูกค้า การดำเนินงาน และอุปกรณ์ Internet of Things (IoT) จะไหลเข้ามายังแหล่งเดียว มีโอกาสสำหรับลูปผลป้อนกลับดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="90884-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="90884-106">เพื่อให้บรรลุประสบการณ์นี้ การรวมระหว่างแอป Finance and Operations และแอปพลิเคชัน Dynamics 365 อื่น ๆ เป็นสิ่งจำเป็น</span><span class="sxs-lookup"><span data-stu-id="90884-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="90884-107">แอพลิเคชันบางส่วนถูกสร้างขึ้นบน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90884-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="90884-108">การรวมระหว่างข้อมูลแอป Finance and Operations กับ Common Data Service ทำให้แอพพลิเคชันอื่นๆสื่อสารในลักษณะที่สอดคล้องกันและราบรื่นกับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="90884-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="90884-109">แอป Finance and Operations และ Common Data Service จัดเตรียมข้อมูลที่ใกล้เคียงเวลาจริงจากการทำข้อมูลของแอป Finance and Operations และแอปพลิเคชัน Dynamics 365 อื่น ๆ ให้ตรงกันผ่านกรอบงาน Dual Write</span><span class="sxs-lookup"><span data-stu-id="90884-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="90884-110">ความครอบคลุมกว้างและครอบคลุมถึง 28 พื้นที่ผิวของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="90884-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="90884-111">เป้าหมายคือเพื่อให้ประสบการณ์ผู้ใช้งาน "Dynamics 365 หนึ่งรายการ" ผ่านโฟลว์ข้อมูลแบบราบรื่นที่เชื่อมต่อกระบวนการทางธุรกิจระหว่างแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="90884-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![ไดอะแกรมภาพรวมของสถาปัตยกรรม](media/dual-write-overview.jpg)

<span data-ttu-id="90884-113">ข้อเสนอของค่าต่อไปนี้จะพร้อมใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="90884-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="90884-114">ลำดับชั้นขององค์กรใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90884-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="90884-115">แนวคิดของบริษัทใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90884-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="90884-116">ข้อมูลหลักของลูกค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="90884-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="90884-117">บัญชีแยกประเภทที่รวม</span><span class="sxs-lookup"><span data-stu-id="90884-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="90884-118">ประสบการณ์ใช้งานผลิตภัณฑ์แบบครบวงจร</span><span class="sxs-lookup"><span data-stu-id="90884-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="90884-119">ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม</span><span class="sxs-lookup"><span data-stu-id="90884-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="90884-120">ไซต์และคลังสินค้าแบบรวม</span><span class="sxs-lookup"><span data-stu-id="90884-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="90884-121">ข้อมูลหลักของภาษีรวม</span><span class="sxs-lookup"><span data-stu-id="90884-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="90884-122">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="90884-122">System requirements</span></span>

<span data-ttu-id="90884-123">โฟลว์ข้อมูลแบบใกล้เรียลไทม์ สองทิศทาง แบบซิงโครนัส จำเป็นต้องมีรุ่นต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="90884-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="90884-124">Microsoft Dynamics 365 for Finance and Operations รุ่น 10.0.4 (กรกฎาคม 2019) ที่มีการปรับปรุงแพลตฟอร์ม 28 หรือสูงกว่า</span><span class="sxs-lookup"><span data-stu-id="90884-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="90884-125">Microsoft Dynamics 365 for Customer Engagement รุ่นแพลตฟอร์ม 9.1 (4.2) หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="90884-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="90884-126">คำแนะนำในการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="90884-126">Setup instructions</span></span>

<span data-ttu-id="90884-127">ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าการรวมระหว่างแอป Finance and Operations กับ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="90884-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="90884-128">สำหรับการตั้งค่าของระบบการเขียนแบบคู่ ให้ดูที่ [คำแนะนำทีละขั้นตอน](https://aka.ms/dualwrite-docs) ในการประกาศการแสดงตัวอย่างการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="90884-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="90884-129">ดาวน์โหลดและติดตั้งโซลูชันจากกลุ่ม [การรวม Fin Ops และ CDS/CE โดย Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer</span><span class="sxs-lookup"><span data-stu-id="90884-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="90884-130">แพคเกจประกอบด้วยโซลูชันห้ารายการ:</span><span class="sxs-lookup"><span data-stu-id="90884-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="90884-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="90884-131">Dynamics365Company</span></span>
    + <span data-ttu-id="90884-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="90884-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="90884-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="90884-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="90884-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="90884-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="90884-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="90884-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="90884-136">ทำตามลำดับการดำเนินการสำหรับ [การซิงโครไนซ์ข้อมูลอ้างอิงเริ่มต้น](initial-sync.md)</span><span class="sxs-lookup"><span data-stu-id="90884-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="90884-137">หากคุณพบปัญหาการซิงโครไนส์การเขียนแบบคู่ ให้ดูที่ [คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล](dual-write-troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="90884-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90884-138">คุณไม่สามารถเรียกใช้การเขียนแบบคู่และ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](../../../../supply-chain/sales-marketing/prospect-to-cash.md) แบบเคียงข้างกันได้</span><span class="sxs-lookup"><span data-stu-id="90884-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="90884-139">ถ้าคุณกำลังเรียกใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องถอนการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="90884-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="90884-140">นอกจากนี้ คุณต้องปิดใช้งานเท็มเพลตการเขียนแบบคู่ของลูกค้าและผู้จัดจำหน่ายที่เป็นส่วนหนึ่งของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="90884-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
