---
title: ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง
description: หัวข้อนี้มีข้อมูลเกี่ยวกับการแก้ไขปัญหาค่าฟิลด์ที่ไม่ถูกต้องใน TaxTrans
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947714"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="15ff2-103">ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="15ff2-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15ff2-104">ถ้าค่าฟิลด์ใน **TaxTrans** ไม่ถูกต้อง ให้ใช้ข้อมูลในหัวข้อนี้เพื่อลองแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="15ff2-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="15ff2-105">ภาพรวมของค่า</span><span class="sxs-lookup"><span data-stu-id="15ff2-105">Overview of values</span></span>
<span data-ttu-id="15ff2-106">รายการต่อไปนี้แสดงวิธี **TaxTrans** **TaxUncommitted** และ **TmpTaxWorkTrans** เป็นชุดข้อมูลที่คล้ายกัน แต่อยู่ในงานต่างกัน</span><span class="sxs-lookup"><span data-stu-id="15ff2-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="15ff2-107">**TaxTrans** เป็นผลลัพธ์ธุรกรรมภาษีที่ลงรายการบัญชีขั้นสุดท้ายที่ยังคงอยู่ในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="15ff2-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="15ff2-108">**TaxUncommitted** เป็นผลลัพธ์ภาษีที่คํานวณได้ระหว่างกลางที่ยังคงอยู่ในฐานข้อมูล (ถ้าเกี่ยวข้อง) ซึ่งจะใช้ในภายหลังในการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="15ff2-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="15ff2-109">**TmpTaxWorkTrans** เป็นภาษีที่คํานวณชั่วคราวที่คํานวณได้ในตารางในหน่วยความจํา (ชนิดตาราง = InMemory)</span><span class="sxs-lookup"><span data-stu-id="15ff2-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="15ff2-110">หากคุณพบสาเหตุรากของคอลัมน์ **TaxTrans** ที่ไม่ถูกต้อง คุณจะพบสาเหตุรากของคอลัมน์ **TaxUncommitted** หรือ **TmpTaxWorkTrans** ที่ไม่ถูกต้องด้วย</span><span class="sxs-lookup"><span data-stu-id="15ff2-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="15ff2-111">เนื่องจากแต่ละคอลัมน์คัดลอกจากกันและกัน</span><span class="sxs-lookup"><span data-stu-id="15ff2-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="15ff2-112">โดยทั่วไปในระหว่างการคํานวณภาษี **TmpTaxWorkTrans** จะมีการสร้าง แล้วระบบจะสร้าง **TaxUncommitted** ถ้าเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="15ff2-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="15ff2-113">ระหว่างการลงรายการบัญชีภาษี **TaxTrans** จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="15ff2-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="15ff2-114">เพิ่มจุดสั่งหยุด</span><span class="sxs-lookup"><span data-stu-id="15ff2-114">Add breakpoints</span></span>
<span data-ttu-id="15ff2-115">หากต้องการเพิ่มจุดสั่งหยุด โปรดทำตามขั้นตอนต่อไปนี้ให้ครบถ้วน:</span><span class="sxs-lookup"><span data-stu-id="15ff2-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="15ff2-116">เพิ่มส่วนขยายและจุดสั่งหยุดใน *insert()* และ *update()* ในส่วนขยายดังที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="15ff2-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="15ff2-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="15ff2-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="15ff2-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="15ff2-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="15ff2-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="15ff2-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="15ff2-120">หรือคุณสามารถเพิ่มจุดสั่งหยุดโดยตรงเมื่อ **TaxUncommitted** ไม่ถูกรวมไว้</span><span class="sxs-lookup"><span data-stu-id="15ff2-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="15ff2-121">*TaxTrans.insert()* *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="15ff2-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="15ff2-122">*TmpTaxWorkTrans.insert()* *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="15ff2-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="15ff2-123">การสร้างอีกครั้งและการดีบัก</span><span class="sxs-lookup"><span data-stu-id="15ff2-123">Reproduce and debug</span></span>

<span data-ttu-id="15ff2-124">หลังจากตั้งค่าจุดสั่งหยุดแล้ว การเปลี่ยนแปลงการยังคงอยู่ของข้อมูลทั้งหมดจะปรากฏในระหว่างการดีบัก</span><span class="sxs-lookup"><span data-stu-id="15ff2-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="15ff2-125">เมื่อต้องการค้นหาสาเหตุรากของคอลัมน์ที่ไม่ถูกต้องของ **TaxTrans** **TaxUncommitted** หรือ **TmpTaxWorkTrans** ให้ตรวจทานและจดบันทึกรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="15ff2-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="15ff2-126">จุดสั่งหยุดสุดท้ายที่คอลัมน์ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="15ff2-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="15ff2-127">จุดสั่งหยุดแรกที่คอลัมน์ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="15ff2-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="15ff2-128">สิ่งที่เกิดขึ้นระหว่างสองจุดดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="15ff2-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="15ff2-129">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="15ff2-129">Determine whether customization exists</span></span>
<span data-ttu-id="15ff2-130">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ยังไม่สามารถแก้ไขปัญหาได้ ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="15ff2-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="15ff2-131">ถ้าไม่มีการกำหนดเอง โปรดติดต่อฝ่ายสนับสนุนของ Microsoft เพื่อขอความช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="15ff2-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

