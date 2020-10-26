---
title: จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)
description: หัวข้อนี้อธิบายวิธีการจัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 28abef376e8462c9a69dbd8e5033ea799b6a4b3a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977826"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="3d9aa-103">จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)</span><span class="sxs-lookup"><span data-stu-id="3d9aa-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d9aa-104">การตรวจสอบ International Bank Account Number (IBAN) เพิ่มจำนวนการตรวจสอบที่เสร็จสิ้นแล้ว เมื่อคุณเพิ่ม IBAN ไปยังบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d9aa-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="3d9aa-105">ข้อมูลเกี่ยวกับโครงสร้างของ IBAN ถูกจัดเก็บใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="3d9aa-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="3d9aa-106">ข้อมูลดังกล่าวถูกโหลดโดยอัตโนมัติ เมื่อคุณใช้ IBAN สำหรับบัญชีธนาคารเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="3d9aa-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="3d9aa-107">ประกอบด้วยความยาวของ IBAN ตำแหน่งเริ่มต้นของหมายเลขบัญชีธนาคาร และหมายเลขเส้นทาง และความยาวของหมายเลขบัญชีธนาคารและหมายเลขเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="3d9aa-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="3d9aa-108">ตั้งค่าโครงสร้าง IBAN</span><span class="sxs-lookup"><span data-stu-id="3d9aa-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="3d9aa-109">ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> โครงสร้าง IBAN**</span><span class="sxs-lookup"><span data-stu-id="3d9aa-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="3d9aa-110">โปรดสังเกตว่า โครงสร้าง IBAN สำหรับแต่ละประเทศหรือภูมิภาคถูกตั้งค่าไว้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3d9aa-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="3d9aa-111">ถ้าคุณต้องการกำหนดโครงสร้างสำหรับประเทศหรือภูมิภาคบางแห่ง คุณสามารถแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="3d9aa-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="3d9aa-112">คำนิยามโครงสร้างจะเป็นส่วนหนึ่งของรุ่นใหม่แต่ละรุ่น</span><span class="sxs-lookup"><span data-stu-id="3d9aa-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="3d9aa-113">คุณสามารถใช้เมนู **รีเซ็ตโครงสร้าง** เพื่อโหลดนิยามล่าสุด หลังการปรับปรุงแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="3d9aa-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="3d9aa-114">ตรวจสอบความถูกต้องของโครงสร้างทางบัญชี IBAN ในบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d9aa-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="3d9aa-115">ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="3d9aa-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="3d9aa-116">สร้างบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d9aa-116">Create a bank account.</span></span>
3. <span data-ttu-id="3d9aa-117">บน FastTab **ข้อมูลเพิ่มเติม** ป้อน IBAN</span><span class="sxs-lookup"><span data-stu-id="3d9aa-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="3d9aa-118">ถ้าความยาวของ IBAN ไม่ตรงกับความยาวที่กำหนดไว้สำหรับแต่ละประเทศหรือภูมิภาค คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="3d9aa-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="3d9aa-119">คุณไม่สามารถทำต่อไปได้ ถ้าความยาวของ IBAN ไม่ตรงกับความยาวที่ระบุในโครงสร้างของ IBAN</span><span class="sxs-lookup"><span data-stu-id="3d9aa-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="3d9aa-120">การตรวจสอบจะยังสามารถตรวจสอบว่า หมายเลขบัญชีธนาคารให้ตรงกับส่วนของ IBAN ที่แสดงถึงหมายเลขบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="3d9aa-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="3d9aa-121">ถ้าหมายเลขบัญชีธนาคารไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="3d9aa-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="3d9aa-122">ข้อความนี้เป็นเพียงคำเตือนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3d9aa-122">This message is only a warning.</span></span> <span data-ttu-id="3d9aa-123">คุณสามารถดำเนินต่อไปได้ แม้ว่าหมายเลขบัญชีธนาคารจะไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="3d9aa-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="3d9aa-124">การตรวจสอบจะยังตรวจสอบว่า หมายเลขการกำหนดเส้นทางธนาคารตรงกับส่วนของ IBAN ที่แสดงถึงหมายเลขการกำหนดเส้นทางธนาคารอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="3d9aa-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="3d9aa-125">หมายเลขการกำหนดเส้นทางรวมหมายเลขธนาคาร และมักจะมีสาขาธนาคารเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="3d9aa-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="3d9aa-126">ถ้าหมายเลขการกำหนดเส้นทางธนาคารไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="3d9aa-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="3d9aa-127">ข้อความนี้เป็นเพียงคำเตือนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3d9aa-127">This message is only a warning.</span></span> <span data-ttu-id="3d9aa-128">คุณสามารถดำเนินต่อไปได้ แม้ว่าหมายเลขการกำหนดเส้นทางธนาคารจะไม่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="3d9aa-128">You can continue even if the bank routing number doesn't match.</span></span>
