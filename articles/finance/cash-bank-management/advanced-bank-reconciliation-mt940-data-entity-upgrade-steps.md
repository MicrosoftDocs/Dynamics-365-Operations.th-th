---
title: การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม
description: ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91100c3e3c33462e5b19ca239a784cdb720210ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772018"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="09cc3-103">การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="09cc3-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09cc3-104">ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940</span><span class="sxs-lookup"><span data-stu-id="09cc3-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="09cc3-105">ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940</span><span class="sxs-lookup"><span data-stu-id="09cc3-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="09cc3-106">คอมไพล์และซิงโครไนส์รายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="09cc3-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="09cc3-107">เอนทิตี้แบบรวม\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="09cc3-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="09cc3-108">เอนทิตี้\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="09cc3-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="09cc3-109">เอนทิตี้\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="09cc3-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="09cc3-110">เอนทิตี้\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="09cc3-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="09cc3-111">เอนทิตี้\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="09cc3-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="09cc3-112">ตาราง\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="09cc3-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="09cc3-113">การจัดการข้อมูล\\โครงการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="09cc3-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="09cc3-114">โครงการการนำเข้า MT940 ของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="09cc3-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="09cc3-115">เปลี่ยน XSLT</span><span class="sxs-lookup"><span data-stu-id="09cc3-115">Change XSLT.</span></span>
            -   <span data-ttu-id="09cc3-116">คลิก **ดูแผนที่**</span><span class="sxs-lookup"><span data-stu-id="09cc3-116">Click **View map**.</span></span>
            -   <span data-ttu-id="09cc3-117">คลิก **ดูแผนที่** บนเอกสารใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="09cc3-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="09cc3-118">คลิก **การแปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="09cc3-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="09cc3-119">ลบไฟล์ BankReconiliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="09cc3-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="09cc3-120">เพิ่ม BankReconiliation-to-Composite.xsl เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="09cc3-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="09cc3-121">แสดงข้อมูล **หมายเลขลำดับ** ในโครงร่าง **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="09cc3-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="09cc3-122">รูปแบบข้อมูลต้นทาง = XML-Element</span><span class="sxs-lookup"><span data-stu-id="09cc3-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="09cc3-123">ชื่อเอนทิตี้ = ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="09cc3-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="09cc3-124">อัพโหลดไฟล์ข้อมูล = SampleBankCompositeEntity.xml เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="09cc3-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="09cc3-125">คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="09cc3-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="09cc3-126">คลิก **ใช่** เพื่อสร้างการแม็ปใหม่</span><span class="sxs-lookup"><span data-stu-id="09cc3-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="09cc3-127">ตรวจสอบว่ามีการแม็ป S**equenceNumber**</span><span class="sxs-lookup"><span data-stu-id="09cc3-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="09cc3-128">คลิก **ดูแผนที่** บนเอนทิตี้ใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="09cc3-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="09cc3-129">ตรวจสอบว่ามีการแม็ป **SequenceNumber** จากต้นทางไปยังการแบ่งระยะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="09cc3-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="09cc3-130">นำเข้าใบแจ้งยอดใหม่</span><span class="sxs-lookup"><span data-stu-id="09cc3-130">Import the new statement.</span></span>




