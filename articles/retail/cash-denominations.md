---
title: ตั้งค่าคอนฟิกหน่วยเงินของเงินสดสำหรับการขายหน้าร้าน (POS)
description: คุณสามารถกำหนดหน่วยเงินของเงินสดสำหรับธนบัตรและเหรียญได้ที่ฝ่ายสนับสนุนให้ถูกนำไปใช้โดยพนักงานเก็บเงิน สมาคมการขาย และผู้จัดการที่ร้านค้าจากภายใน POS
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 24775044e5a502a5615392a6a8c4030bdfafb0ab
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "343523"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a><span data-ttu-id="e01ca-103">ตั้งค่าคอนฟิกหน่วยเงินของเงินสดสำหรับการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="e01ca-103">Configure cash denominations for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e01ca-104">คุณสามารถกำหนดหน่วยเงินของเงินสดสำหรับธนบัตรและเหรียญได้ที่ฝ่ายสนับสนุนให้ถูกนำไปใช้โดยพนักงานเก็บเงิน สมาคมการขาย และผู้จัดการที่ร้านค้าจากภายใน POS</span><span class="sxs-lookup"><span data-stu-id="e01ca-104">Cash denominations for notes and coins can be defined in the back office to be used by cashiers, sales associates, and managers at the store from within the POS.</span></span> <span data-ttu-id="e01ca-105">คุณสามารถใช้หน่วยเงินเหล่านี้เพื่อช่วยในการตรวจนับเงินสดสำหรับการตรวจนับเงินในช่วงท้ายของวันหรือเพื่อให้สามารถชำระเงินการขายได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="e01ca-105">These denominations can be used to aid in counting cash for end of day tender declarations or for quickly tendering a sale.</span></span>

## <a name="define-denominations"></a><span data-ttu-id="e01ca-106">กำหนดหน่วยเงิน</span><span class="sxs-lookup"><span data-stu-id="e01ca-106">Define denominations</span></span>

<span data-ttu-id="e01ca-107">หน่วยเงินจะถูกตั้งค่าสำหรับแต่ละร้านค้าในหน้า **ตั้งค่า** \> **ตัวเลือกการตรวจนับเงินสดจากคุณสมบัติร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="e01ca-107">The denominations are set up per store on the **Set up** \> **Cash declaration option from the store property** page.</span></span>

![หน่วยเงินของเงินสด](./media/image1-denomination.png)

<span data-ttu-id="e01ca-109">เมื่อต้องการกำหนดหน่วยเงิน:</span><span class="sxs-lookup"><span data-stu-id="e01ca-109">To define a denomination:</span></span>

1. <span data-ttu-id="e01ca-110">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e01ca-110">Click **New**.</span></span>
1. <span data-ttu-id="e01ca-111">ระบุชนิด (เหรียญหรือธนบัตร)</span><span class="sxs-lookup"><span data-stu-id="e01ca-111">Specify the type (coin or note).</span></span>
1. <span data-ttu-id="e01ca-112">ระบุจำนวนเงิน (ค่า)</span><span class="sxs-lookup"><span data-stu-id="e01ca-112">Specify the amount (value).</span></span>

![หน่วยเงินของเงินสด](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a><span data-ttu-id="e01ca-114">ตั้งค่าคอนฟิกโพรไฟล์ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="e01ca-114">Configure the functionality profile</span></span>

<span data-ttu-id="e01ca-115">เมื่อชำระเงินด้วยเงินสดใน POS ผู้ใช้สามารถใช้หน่วยเงินของธนบัตรเพื่อป้อนยอดเงินที่ชำระโดยลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="e01ca-115">When paying by cash in POS, the user can use the note denominations to quickly enter the amount paid by the customer.</span></span> <span data-ttu-id="e01ca-116">ในโพรไฟล์ฟังก์ชัน คุณสามารถตั้งค่าคอนฟิกตัวเลือกสองตัวสำหรับการแสดงหน่วยเงินใน POS</span><span class="sxs-lookup"><span data-stu-id="e01ca-116">In the functionality profile, you can configure the two options for showing the denomination in POS.</span></span>

- <span data-ttu-id="e01ca-117">**มากกว่าหรือเท่ากับจำนวนที่ครบกำหนด** – โดยค่าเริ่มต้น POS จะแสดงเฉพาะหน่วยเงินของธนบัตรที่มีมูลค่ามากกว่าจำนวนที่ครบกำหนด ซึ่งอนุญาตให้การชำระเงินแบบสัมผัสเดียว</span><span class="sxs-lookup"><span data-stu-id="e01ca-117">**Greater or equal to amount due** – By default, POS will only show the note denominations that are greater than the amount due, which allows for one-touch tendering.</span></span> <span data-ttu-id="e01ca-118">ตัวอย่างเช่น ถ้าจำนวนที่ครบกำหนดคือ $7.50 POS จะแสดงหน่วยต่อไปนี้: $10, $20, $50 และ $100</span><span class="sxs-lookup"><span data-stu-id="e01ca-118">For example, if the amount due is $7.50, POS would show the following denominations: $10, $20, $50, and $100.</span></span> <span data-ttu-id="e01ca-119">การสัมผัสจำนวนใด ๆ เหล่านี้จะเป็นการชำระเงินการขายสำหรับจำนวนนั้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e01ca-119">Touching any of these amounts will automatically tender the sale for that amount.</span></span> <span data-ttu-id="e01ca-120">ธนบัตร $1 และ $5 จะไม่ถูกแสดงเนื่องจากจำนวนเหล่านี้มีค่าน้อยกว่าจำนวนที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="e01ca-120">The $1 and $5 notes are not shown since these amounts are less than the amount due.</span></span>
- <span data-ttu-id="e01ca-121">**หน่วยเงินทั้งหมด** – เลือกตัวเลือกนี้เพื่อแสดงหน่วยเงินของธนบัตรทั้งหมดใน POS โดยไม่คำนึงถึงจำนวนที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="e01ca-121">**All denominations** – Select this option to always show all note denominations in POS, regardless of the amount due.</span></span> <span data-ttu-id="e01ca-122">ซึ่งหมายความว่าผู้ใช้สามารถใช้ชุดของธนบัตรเพื่อไปถึงจำนวนที่ครบกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="e01ca-122">This means that the user can use a combination of notes to reach the amount due.</span></span> <span data-ttu-id="e01ca-123">ตัวอย่างเช่น ถ้าจำนวนที่ครบกำหนดคือ $25.00 ผู้ใช้สามารถเลือก $20 และ $5 เพื่อทำให้การขายเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="e01ca-123">For example, if the amount due is $25.00, the user can choose $20 and $5 to complete the sale.</span></span>
