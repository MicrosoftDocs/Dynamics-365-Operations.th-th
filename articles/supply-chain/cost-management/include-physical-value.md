---
title: รวมมูลค่าจริง
description: คุณใช้กล่องกาเครื่องหมายรวมมูลค่าจริงในแบบจำลองสินค้าคงคลังของหน้ากลุ่มแบบจำลองสินค้าจะใช้ในการระบุว่ามีการพิจารณาธุรกรรมอัพเดตจริงในการพิจารณาราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับสินค้า
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96d5e2a658a027d66663868329cf4eedcb1d46f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "357323"
---
# <a name="include-physical-value"></a><span data-ttu-id="4093f-103">รวมมูลค่าจริง</span><span class="sxs-lookup"><span data-stu-id="4093f-103">Include physical value</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4093f-104">คุณใช้กล่องกาเครื่องหมายรวมมูลค่าจริงในแบบจำลองสินค้าคงคลังของหน้ากลุ่มแบบจำลองสินค้าจะใช้ในการระบุว่ามีการพิจารณาธุรกรรมอัพเดตจริงในการพิจารณาราคาต้นทุนเฉลี่ยสืบเนื่องสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="4093f-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="4093f-105">กล่องกาเครื่องหมาย **รวมมูลค่าจริง** มีค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4093f-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="4093f-106">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="4093f-106">Value</span></span>    | <span data-ttu-id="4093f-107">ผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="4093f-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4093f-108">เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="4093f-108">Selected</span></span> | <span data-ttu-id="4093f-109">ทั้งธุรกรรมทางกายภาพและที่ได้รับการอัพเดตตามจริงและทางการเงินถูกนำมาใช้ในการคำนวณราคาต้นทุนเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="4093f-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="4093f-110">ล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4093f-110">Cleared</span></span>  | <span data-ttu-id="4093f-111">เฉพาะธุรกรรมที่มีการอัพเดตทางการเงินจะใช้สำหรับหาราคาต้นทุนเฉลี่ย</span><span class="sxs-lookup"><span data-stu-id="4093f-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="4093f-112">กล่องกาเครื่องหมายมีลักษณะแตกต่างกันเล็กน้อย ขึ้นอยู่กับรูปแบบจำลองสินค้าคงคลังที่คุณใช้</span><span class="sxs-lookup"><span data-stu-id="4093f-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="4093f-113">ถ้าคุณเลือกกล่องกาเครื่องหมาย **รวมมูลค่าจริง** เมื่อคุณใช้ FIFO (เข้าก่อน ออกก่อน), LIFO (เข้าหลัง ออกก่อน) หรือ แบบจำลองสินค้าคงคลังของวันที่แบบ LIFO การปิดสินค้าคงคลังยังช่วยให้การปรับปรุงธุรกรรมมีการอัพเดตทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="4093f-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="4093f-114">ถ้าคุณไม่เลือกกล่องกาเครื่องหมาย **รวมมูลค่าทางกายภาพ** เมื่อใช้แบบจำลองสินค้าคงคลัง การปิดสินค้าคงคลังจะชำระเฉพาะธุรกรรมที่มีการอัพเดตทางการเงินเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4093f-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="4093f-115">เมื่อคุณใช้ค่าเฉลี่ยถ่วงน้ำหนักหรือแบบจำลองสินค้าคงคลังของวันที่ค่าเฉลี่ยถ่วงน้ำหนัก แบบจำลองการปิดสินค้าคงคลังจะชำระเฉพาะธุรกรรมที่ได้รับการอัพเดตทางการเงิน ไม่ว่าคุณได้เลือกกล่องกาเครื่องหมาย **รวมมูลค่าจริง** หรือไม่ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="4093f-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="4093f-116">**ตัวอย่างที่ 1** คุณเลือกกล่องกาเครื่องหมาย**รวมมูลค่าจริง** และรับใบสั่งซื้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4093f-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="4093f-117">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 2 หน่วย และราคาต่อหน่วย USD 10.00 ที่มีการอัพเดตบันทึกการจัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="4093f-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="4093f-118">ระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 3 หน่วย และราคาต่อหน่วย USD 12.00 ที่มีการอัพเดตใบแจ้งหนี้แล้ว</span><span class="sxs-lookup"><span data-stu-id="4093f-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="4093f-119">ในกรณีนี้ ราคาต้นทุนค่าเฉลี่ยสืบเนื่อง คือ 11.20 เหรียญสหรัฐ เนื่องจากทั้งธุรกรรมที่ได้รับการอัพเดตตามจริงและทางการเงินถูกนำมาใช้ในการคำนวณราคาต้นทุน</span><span class="sxs-lookup"><span data-stu-id="4093f-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="4093f-120">**ตัวอย่างที่ 2** คุณไม่ได้เลือกกล่องกาเครื่องหมาย **รวมมูลค่าจริง** และราคาต้นทุนในการตั้งค่าสินค้าคือ 10.00 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="4093f-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="4093f-121">คุณได้รับระบบได้ออกใบแจ้งหนี้สำหรับใบสั่งซื้อปริมาณ 20 หน่วย และราคาต่อหน่วย USD 12.00 ที่มีการอัพเดตบันทึกการจัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="4093f-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="4093f-122">เมื่อใบสั่งขายถูกลงรายการบัญชี จะลงรายการบัญชียอดเงินต้นทุนไว้ที่ 10.00 เหรียญสหรัฐ เนื่องจากราคาต้นทุนค่าเฉลี่ยสืบเนื่องจะไม่รวมธุรกรรมที่ได้รับการลงรายการบัญชีตามจริงเอาไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="4093f-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="4093f-123">**หมายเหตุ:** สำหรับการเปรียบเทียบ ถ้าคุณเลือกกล่องกาเครื่องหมาย **รวมมูลค่าจริง** สำหรับสินค้านี้ เมื่อลงรายการบัญชีใบสั่งขาย ยอดต้นทุนที่ลงรายการบัญชีแล้วจะเป็น 12.00 เหรียญสหรัฐ</span><span class="sxs-lookup"><span data-stu-id="4093f-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>



