---
title: สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้
description: หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585553"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="4d20f-103">สามารถเช็คเอาท์สินค้าที่ไม่มีสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="4d20f-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d20f-104">หัวข้อนี้มีแนวทางการแก้ไขปัญหาเบื้องต้นซึ่งสามารถช่วยเหลือเมื่อลูกค้าสามารถเพิ่มสินค้าที่ไม่มีในสต็อกลงในรถเข็นแล้วเช็คเอาท์ต่อไป</span><span class="sxs-lookup"><span data-stu-id="4d20f-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="4d20f-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="4d20f-105">Description</span></span>

<span data-ttu-id="4d20f-106">ผู้ใช้สามารถเพิ่มสินค้าลงในรถเข็นได้ แม้ว่าจะไม่มีสินค้าคงคลังคงเหลือในร้านค้า แล้วดําเนินการต่อไปยังหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="4d20f-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="4d20f-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="4d20f-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="4d20f-108">เปิดใช้งานคุณสมบัติแสดงข้อผิดพลาดสินค้าคงคลังในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="4d20f-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="4d20f-109">เปิดใช้งานคุณสมบัติ **แสดงข้อผิดพลาดไม่มีสินค้าในสต็อก** ในโปรแกรมสร้างไซต์ Commerce ตามขั้นตอนดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4d20f-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d20f-110">เลือกไซต์ที่คุณพยายามใช้</span><span class="sxs-lookup"><span data-stu-id="4d20f-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="4d20f-111">ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **หน้า**</span><span class="sxs-lookup"><span data-stu-id="4d20f-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="4d20f-112">เลือก **CartPage** เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="4d20f-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="4d20f-113">เลือกช่อง **รถเข็น 1** เลือก **แก้ไข** จากนั้นในบานหน้าต่างคุณสมบัติ ให้เลือกกล่องกาเครื่องหมาย **แสดงข้อผิดพลาดไม่มีสินค้าในสต็อก**</span><span class="sxs-lookup"><span data-stu-id="4d20f-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="4d20f-114">บันทึกและเผยแพร่หน้า</span><span class="sxs-lookup"><span data-stu-id="4d20f-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d20f-115">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d20f-115">Additional resources</span></span>

[<span data-ttu-id="4d20f-116">ใช้การตั้งค่าสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4d20f-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="4d20f-117">คำนวณความพร้อมของสินค้าคงคลังสำหรับช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="4d20f-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="4d20f-118">ตั้งค่าคอนฟิกสินค้าคงคลังสำรองและระดับสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="4d20f-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
