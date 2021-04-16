---
title: อัพเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร
description: จำเป็นต้องดำเนินตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819620"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="9c340-103">อัพเดตเอนทิตี้โดยรวมของสมุดรายวันธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9c340-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c340-104">จำเป็นต้องดำเนินตามขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม</span><span class="sxs-lookup"><span data-stu-id="9c340-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="9c340-105">ใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มฟิลด์ BankTransactionType เพิ่มเติมไปยัง BankJournalEntity โดยรวม</span><span class="sxs-lookup"><span data-stu-id="9c340-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="9c340-106">คอมไพล์และซิงโครไนส์เอนทิตี้โดยรวมของสมุดรายวันธนาคาร เอนทิตี้ และตารางการจัดเตรียมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9c340-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="9c340-107">เอนทิตี้แบบรวม\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="9c340-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="9c340-108">เอนทิตี้\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="9c340-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="9c340-109">เอนทิตี้\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="9c340-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="9c340-110">ตาราง\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="9c340-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="9c340-111">ตาราง\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="9c340-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="9c340-112">การจัดการข้อมูล\\โครงการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9c340-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="9c340-113">แสดงข้อมูลชนิด **ธุรกรรมธนาคาร** บนโครงร่าง **ข้อมูลต้นทาง**</span><span class="sxs-lookup"><span data-stu-id="9c340-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="9c340-114">รูปแบบข้อมูลต้นทาง = XML-Element</span><span class="sxs-lookup"><span data-stu-id="9c340-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="9c340-115">ชื่อเอนทิตี้ = สมุดรายวันธนาคาร</span><span class="sxs-lookup"><span data-stu-id="9c340-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="9c340-116">อัพโหลดไฟล์ข้อมูล = SampleBankJournalCompositeEntity.xml เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="9c340-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="9c340-117">คลิก **ใช่** เพื่อบันทึกทับไฟล์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="9c340-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="9c340-118">คลิก **ใช่** เพื่อสร้างการแม็ปตั้งแต่ต้น</span><span class="sxs-lookup"><span data-stu-id="9c340-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="9c340-119">ตรวจสอบว่ามีการแม็ปชนิดธุรกรรมธนาคารหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9c340-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="9c340-120">คลิก **ดูแผนที่** บนเอนทิตี้ของรายการ</span><span class="sxs-lookup"><span data-stu-id="9c340-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="9c340-121">ตรวจสอบว่ามีการแม็ปชนิดธุรกรรมธนาคารจากต้นทางไปยังการแบ่งระยะหรือไม่</span><span class="sxs-lookup"><span data-stu-id="9c340-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="9c340-122">นำเข้าใบแจ้งยอดใหม่</span><span class="sxs-lookup"><span data-stu-id="9c340-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]