---
title: การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม
description: ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "343799"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="9f776-103">การนำเข้า MT940 การกระทบยอดบัญชีธนาคารขั้นสูง – การอัพเกรดเอนทิตี้ข้อมูลแบบรวม</span><span class="sxs-lookup"><span data-stu-id="9f776-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f776-104">ต้องมีหมายเลขลำดับที่จะเพิ่มลงในเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940</span><span class="sxs-lookup"><span data-stu-id="9f776-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="9f776-105">ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มเอนทิตี้การนำเข้าใบแจ้งยอดจากธนาคารเพื่อสนับสนุนรูปแบบ MT940</span><span class="sxs-lookup"><span data-stu-id="9f776-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="9f776-106">คอมไพล์และซิงโครไนส์รายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9f776-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="9f776-107">เอนทิตี้แบบรวม\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="9f776-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="9f776-108">เอนทิตี้\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="9f776-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="9f776-109">เอนทิตี้\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="9f776-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="9f776-110">เอนทิตี้\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="9f776-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="9f776-111">เอนทิตี้\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="9f776-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="9f776-112">ตาราง\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="9f776-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="9f776-113">การจัดการข้อมูล\\โครงการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9f776-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="9f776-114">โครงการการนำเข้า MT940 ของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="9f776-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="9f776-115">เปลี่ยน XSLT</span><span class="sxs-lookup"><span data-stu-id="9f776-115">Change XSLT.</span></span>
            -   <span data-ttu-id="9f776-116">คลิก **ดูแผนที่**</span><span class="sxs-lookup"><span data-stu-id="9f776-116">Click **View map**.</span></span>
            -   <span data-ttu-id="9f776-117">คลิก **ดูแผนที่** บนเอกสารใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f776-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="9f776-118">คลิก **การแปลงข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9f776-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="9f776-119">ลบไฟล์ BankReconiliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="9f776-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="9f776-120">เพิ่ม BankReconiliation-to-Composite.xsl เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="9f776-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="9f776-121">แสดงข้อมูล **หมายเลขลำดับ** ในโครงร่าง **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="9f776-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="9f776-122">รูปแบบข้อมูลต้นทาง = XML-Element</span><span class="sxs-lookup"><span data-stu-id="9f776-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="9f776-123">ชื่อเอนทิตี้ = ใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9f776-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="9f776-124">อัพโหลดไฟล์ข้อมูล = SampleBankCompositeEntity.xml เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="9f776-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="9f776-125">คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9f776-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="9f776-126">คลิก **ใช่** เพื่อสร้างการแม็ปใหม่</span><span class="sxs-lookup"><span data-stu-id="9f776-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="9f776-127">ตรวจสอบว่ามีการแม็ป S**equenceNumber**</span><span class="sxs-lookup"><span data-stu-id="9f776-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="9f776-128">คลิก **ดูแผนที่** บนเอนทิตี้ใบแจ้งยอด</span><span class="sxs-lookup"><span data-stu-id="9f776-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="9f776-129">ตรวจสอบว่ามีการแม็ป **SequenceNumber** จากต้นทางไปยังการแบ่งระยะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9f776-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="9f776-130">นำเข้าใบแจ้งยอดใหม่</span><span class="sxs-lookup"><span data-stu-id="9f776-130">Import the new statement.</span></span>




