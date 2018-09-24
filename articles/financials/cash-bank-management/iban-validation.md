---
title: "จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)"
description: "หัวข้อนี้อธิบายวิธีการจัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)"
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: th-th
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="3fd0a-103">จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)</span><span class="sxs-lookup"><span data-stu-id="3fd0a-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fd0a-104">การตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN) เพิ่มจำนวนการตรวจสอบที่เสร็จสิ้นแล้วเมื่อคุณเพิ่ม IBAN ไปยังบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3fd0a-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="3fd0a-105">โครงสร้างของ IBAN ถูกเก็บไว้ใน Microsoft Dynamics 365 for Finance and Operation และจะถูกโหลดโดยอัตโนมัติเมื่อคุณใช้ IBAN สำหรับบัญชีธนาคารครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="3fd0a-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="3fd0a-106">หมายเลขบัญชีธนาคารเป็นส่วนหนึ่งของโครงสร้างที่กำหนดไว้สำหรับหมายเลข IBAN</span><span class="sxs-lookup"><span data-stu-id="3fd0a-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="3fd0a-107">โดยขึ้นอยู่กับโครงสร้างนั้น ถ้าตำแหน่งและความยาวของหมายเลขบัญชีใน IBAN ไม่ตรงกับตำแหน่งที่กำหนดไว้ในโครงสร้างสำหรับแต่ละประเทศหรือภูมิภาค คุณจะได้รับข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="3fd0a-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="3fd0a-108">ตั้งค่าโครงสร้าง IBAN</span><span class="sxs-lookup"><span data-stu-id="3fd0a-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="3fd0a-109">ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> โครงสร้าง IBAN**</span><span class="sxs-lookup"><span data-stu-id="3fd0a-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="3fd0a-110">โปรดสังเกตว่า โครงสร้าง IBAN สำหรับแต่ละประเทศหรือภูมิภาคถูกตั้งค่าไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3fd0a-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="3fd0a-111">ถ้าคุณต้องกำหนดโครงสร้างสำหรับบางประเทศหรือภูมิภาค คุณสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="3fd0a-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="3fd0a-112">คำนิยามโครงสร้างจะเป็นส่วนหนึ่งของรุ่นใหม่แต่ละรุ่น</span><span class="sxs-lookup"><span data-stu-id="3fd0a-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="3fd0a-113">คุณสามารถใช้เมนู **รีเซ็ตโครงสร้าง** เพื่อโหลดนิยามล่าสุด หลังการปรับปรุงแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="3fd0a-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="3fd0a-114">ตรวจสอบความถูกต้องของโครงสร้างทางบัญชี IBAN ในบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3fd0a-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="3fd0a-115">ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="3fd0a-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="3fd0a-116">สร้างบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3fd0a-116">Create a bank account.</span></span>
3. <span data-ttu-id="3fd0a-117">บน FastTab **ข้อมูลเพิ่มเติม** ป้อน IBAN</span><span class="sxs-lookup"><span data-stu-id="3fd0a-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="3fd0a-118">ถ้าตำแหน่งและความยาวของหมายเลขบัญชีใน IBAN ไม่ตรงกับตำแหน่งที่กำหนดไว้ในโครงสร้างสำหรับแต่ละประเทศหรือภูมิภาค คุณจะได้รับข้อความเตือน</span><span class="sxs-lookup"><span data-stu-id="3fd0a-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="3fd0a-119">คุณไม่สามารถทำต่อไปถ้า ความยาวของ IBAN ไม่ตรงกับความยาวในโครงสร้างของ IBAN</span><span class="sxs-lookup"><span data-stu-id="3fd0a-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="3fd0a-120">การตรวจสอบจะยังสามารถตรวจสอบว่า หมายเลขบัญชีธนาคารให้ตรงกับส่วนของ IBAN ที่แสดงถึงหมายเลขบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3fd0a-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="3fd0a-121">ถ้าหมายเลขบัญชีธนาคารไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="3fd0a-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="3fd0a-122">ข้อความนี้เป็นเพียงคำเตือนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3fd0a-122">This message is only a warning.</span></span> <span data-ttu-id="3fd0a-123">คุณสามารถดำเนินต่อไปได้ แม้ว่าหมายเลขบัญชีธนาคารจะไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="3fd0a-123">You can continue even if the bank account number doesn't match.</span></span>

