---
title: ตั้งค่าชนิดค่าใช้จ่าย
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าชนิดค่าใช้จ่ายในการเช่าสินทรัพย์
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d27c5653d6305aad23142fa6f803134153661278
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448606"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="d98ee-103">ตั้งค่าชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d98ee-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d98ee-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าชนิดค่าใช้จ่ายในการเช่าสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="d98ee-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="d98ee-105">ต้นทุนที่ไม่ได้แสดงไว้โดยกำหนดการชำระเงินจะเรียกว่า *ต้นทุนค่าใช้จ่าย*</span><span class="sxs-lookup"><span data-stu-id="d98ee-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="d98ee-106">ตัวอย่างของต้นทุนเหล่านี้ได้แก่ ภาษีทรัพย์สิน ต้นทุนการบำรุงรักษาพื้นที่ทั่วไป และค่าใช้จ่ายในการประกันภัย</span><span class="sxs-lookup"><span data-stu-id="d98ee-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="d98ee-107">เพิ่มชนิดค่าใช้จ่ายในการบริหารงาน</span><span class="sxs-lookup"><span data-stu-id="d98ee-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="d98ee-108">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> ชนิดค่าใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="d98ee-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="d98ee-109">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="d98ee-109">Select **New**.</span></span>
3. <span data-ttu-id="d98ee-110">ในฟิลด์ที่เหมาะสม ให้ป้อนชนิดค่าใช้จ่ายใหม่และคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d98ee-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="d98ee-111">กำหนดบัญชีให้กับต้นทุนการจัดการ</span><span class="sxs-lookup"><span data-stu-id="d98ee-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="d98ee-112">ถัดไป คุณควรเชื่อมโยงบัญชีที่มีชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d98ee-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="d98ee-113">บัญชีเหล่านี้จะถูกเดบิตเมื่อลงรายการบัญชีรายการกำหนดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d98ee-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="d98ee-114">มีการระบุบัญชีตรงข้ามบนรายการ **กำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์** ในแต่ละสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="d98ee-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="d98ee-115">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="d98ee-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d98ee-116">บนแท็บ **บัญชี** บนแท็บด่วน **ค่าใช้จ่ายในการจัดการสินทรัพย์** ในฟิลด์ **ชนิดค่าใช้จ่าย** ให้เลือกชนิดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d98ee-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="d98ee-117">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d98ee-117">Select **Add**.</span></span>
4. <span data-ttu-id="d98ee-118">ในฟิลด์ **ชนิดสมุดบัญชี** ให้เลือกชนิดของสมุดบัญชีที่จะเชื่อมโยงกับต้นทุนการจัดการ</span><span class="sxs-lookup"><span data-stu-id="d98ee-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d98ee-119">ชนิดของสมุดบัญชีหลายชนิดสามารถเชื่อมโยงกับบัญชีค่าใช้จ่ายเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="d98ee-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="d98ee-120">ในฟิลด์ **รหัสบัญชี** ให้ระบุว่าควรใช้สัญญาเช่าอย่างไรกับสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="d98ee-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="d98ee-121">**ทั้งหมด** – นำสมุดบัญชีไปใช้กับสัญญาเช่าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d98ee-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="d98ee-122">**กลุ่ม** – นำสมุดบัญชีไปใช้กับกลุ่มสัญญาเช่าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d98ee-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="d98ee-123">**ตาราง** – นำสมุดบัญชีไปใช้กับสัญญาเช่าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d98ee-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="d98ee-124">ถ้าคุณเลือก **กลุ่ม** หรือ **ตาราง** ในฟิลด์ **รหัสบัญชี** เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มในฟิลด์ **หมายเลขบัญชี/กลุ่ม**</span><span class="sxs-lookup"><span data-stu-id="d98ee-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="d98ee-125">ในฟิลด์ที่เหมาะสม ให้เลือกบัญชีหลักของสัญญาเช่าทางการเงินและบัญชีหลักของการเช่าดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="d98ee-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="d98ee-126">เมื่อคุณดำเนินการขั้นตอนต่อไปนี้เสร็จสมบูรณ์แล้ว คุณสามารถเพิ่มค่าใช้จ่ายผ่านทางรายการ **กำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์** ในหน้า **รายละเอียดสัญญาเช่า** ของสัญญาเช่าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d98ee-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="d98ee-127">อีกทางหนึ่งคือ คุณสามารถเพิ่มค่าใช้จ่ายเมื่อคุณสร้างสัญญาเช่าใหม่</span><span class="sxs-lookup"><span data-stu-id="d98ee-127">Alternatively, you can add expenses when you create a new lease.</span></span>
