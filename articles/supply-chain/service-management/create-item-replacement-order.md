---
title: การสร้างใบสั่งเปลี่ยนสินค้า
description: 'โดยปกติ ใบสั่งเปลี่ยนสินค้ามีการสร้างขึ้นหลังจากที่มีการส่งคืนและตรวจสอบผลิตภัณฑ์อย่างละเอียดแล้ว '
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0932c34cc6b3604afbea7c8a18620640c00d928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258010"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="b736b-103">การสร้างใบสั่งเปลี่ยนสินค้า</span><span class="sxs-lookup"><span data-stu-id="b736b-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b736b-104">โดยปกติ ใบสั่งเปลี่ยนสินค้ามีการสร้างขึ้นหลังจากที่มีการส่งคืนและตรวจสอบผลิตภัณฑ์อย่างละเอียดแล้ว </span><span class="sxs-lookup"><span data-stu-id="b736b-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="b736b-105">อย่างไรก็ตาม ถ้าต้องเปลี่ยนสินค้าก่อนหน้าที่สินค้านั้นจะถูกส่งคืน หรือถ้าจะไม่มีการส่งคืนสินค้าดั้งเดิม คุณสามารถสร้างใบสั่งเปลี่ยนสินค้าในทันทีหลังจากที่คุณสร้างใบสั่งส่งคืนสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="b736b-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="b736b-106">สร้างใบสั่งเปลี่ยนทดแทนหลังจากที่คุณได้รับสินค้าที่ถูกส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b736b-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="b736b-107">คลิก **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งส่งคืนสินค้า** \> **ใบสั่งส่งคืนสินค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b736b-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="b736b-108">สร้างใบสั่งคืนใหม่ หรือเลือกใบสั่งที่ส่งคืนจากรายการเพื่อเปิดฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2**</span><span class="sxs-lookup"><span data-stu-id="b736b-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="b736b-109">คลิก **รายการส่งคืน** และจากนั้นเลือก **สินค้าที่เปลี่ยนทดแทน**</span><span class="sxs-lookup"><span data-stu-id="b736b-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="b736b-110">เลือกสินค้าที่จะแทนกับสินค้ารับคืน</span><span class="sxs-lookup"><span data-stu-id="b736b-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="b736b-111">ป้อนข้อมูลจำเพาะของสินค้า และจากนั้นคลิก **นำไปใช้**</span><span class="sxs-lookup"><span data-stu-id="b736b-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="b736b-112">คลิก **บันทึกการจัดส่ง** เพื่อสร้างบันทึกการจัดส่งสำหรับใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="b736b-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="b736b-113">ใบสั่งขายถูกสร้างขึ้นสำหรับสินค้าทดแทนที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="b736b-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="b736b-114">หลังจากที่มีการสร้างใบสั่งขายสำหรับสินค้าที่เปลี่ยนทดแทน จะมีการค้นหาข้อตกลงการขายโดยอัตโนมัติ และถ้ามีข้อตกลงการขายที่ใช้ได้ ก็จะนำไปใช้กับใบสั่งขายนั้น</span><span class="sxs-lookup"><span data-stu-id="b736b-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="b736b-115">สร้างใบสั่งเปลี่ยนทดแทนก่อนที่คุณได้รับสินค้าที่จะถูกส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b736b-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="b736b-116">คลิก **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งส่งคืนสินค้า** \> **ใบสั่งส่งคืนสินค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="b736b-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="b736b-117">สร้างใบสั่งคืนใหม่ หรือเลือกใบสั่งส่งคืนจากรายการเพื่อเปิดฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2**</span><span class="sxs-lookup"><span data-stu-id="b736b-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="b736b-118">คลิก **ค้นหาใบสั่งขาย** ถ้าคุณต้องการระบุใบสั่งขายสำหรับสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="b736b-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="b736b-119">ทำให้ฟอร์ม **ค้นหาใบสั่งขาย** เสร็จสมบูรณ์ และจากนั้น คลิก **ตกลง** เพื่อปิดฟอร์ม และส่งคืนไปยังฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2**</span><span class="sxs-lookup"><span data-stu-id="b736b-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="b736b-120">รายการใบสั่งขายสำหรับสินค้ารับคืนถูกคัดลอกไปยังใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="b736b-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="b736b-121">คลิก **ใบสั่งเปลี่ยนทดแทน** เพื่อเปิดฟอร์ม **สร้างใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="b736b-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="b736b-122">เลือกกล่องกาเครื่องหมาย **คัดลอกรายการใบสั่งส่งคืน** เพื่อย้ายรายละเอียดจากใบสั่งส่งคืนที่คุณเลือกในฟอร์ม **ใบสั่งส่งคืน - หมายเลข RMA: %1, %2** ไปยังใบสั่งขายนี้</span><span class="sxs-lookup"><span data-stu-id="b736b-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="b736b-123">ป้อนหรือแก้ไขรายละเอียดตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="b736b-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="b736b-124">ถ้าคุณระบุใบสั่งขายในขั้นตอนที่ 3 และถ้ารายการใบสั่งขายสำหรับสินค้าที่ส่งคืนถูกเชื่อมโยงกับข้อตกลงการขาย ตัวระบุของข้อตกลงการขายที่ใช้ได้สำหรับใบสั่งเปลี่ยนทดแทนสินค้าจะแสดงขึ้นในฟิลด์ **รหัสข้อตกลงการขาย** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="b736b-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="b736b-125">คลิก **ตกลง** เพื่อปิดแบบฟอร์ม **สร้างใบสั่งขาย** และเปิดแบบฟอร์ม **ใบสั่งขาย** ที่ซึ่งคุณสามารถป้อนข้อมูลต่อไปได้สำหรับใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="b736b-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="b736b-126">รายการใบสั่งส่งคืนสินค้าที่เกี่ยวข้องใดๆ จะถูกคัดลอกไปยังใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="b736b-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="b736b-127">ถ้าตัวระบุของข้อตกลงการขายถูกแสดงโดยอัตโนมัติในฟิลด์ **รหัสข้อตกลงการขาย** จากนั้นข้อตกลงการขายได้ถูกเชื่อมโยงไปยังใบสั่งขายสำหรับใบสั่งเปลี่ยนสินค้า</span><span class="sxs-lookup"><span data-stu-id="b736b-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="b736b-128">ถ้ามีข้อผูกมัดที่เกี่ยวข้องในข้อตกลงการขายที่ยังไม่ได้ถูกเติมเต็ม และมีการสร้างใบสั่งขาย ก่อนที่ข้อตกลงการขายจะหมดอายุ จะมีการสร้างลิงค์ระหว่างรายการข้อตกลงการขายและรายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="b736b-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="b736b-129">ดังนั้น ข้อมูลจากข้อตกลงการขาย เช่น ราคาของสินค้า จะถูกคัดลอกไปที่รายการใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="b736b-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]