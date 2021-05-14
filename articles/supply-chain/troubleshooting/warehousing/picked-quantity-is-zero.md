---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938559"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="721c2-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="721c2-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="721c2-104">รหัสข้อผิดพลาด: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="721c2-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="721c2-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="721c2-105">Symptoms</span></span>

<span data-ttu-id="721c2-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="721c2-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="721c2-107">รายการบรรทุกสำหรับสินค้า %1 และการจัดส่ง %2 ได้รับการอัพเดตให้มีปริมาณเป็นศูนย์ เนื่องจากการตั้งค่าการจัดส่งน้อยกว่าปริมาณที่สั่งทำให้ไม่สามารถจัดส่งด้วยปริมาณใดๆ สำหรับสินค้านี้</span><span class="sxs-lookup"><span data-stu-id="721c2-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="721c2-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="721c2-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="721c2-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="721c2-109">Cause</span></span>

<span data-ttu-id="721c2-110">ระบบประเมินว่าปริมาณที่เบิกอยู่ภายในขีดจํากัดที่คาดไว้หรือไม่ ตามปริมาณที่เบิก สินค้าตามปริมาณรายการโหลด และเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="721c2-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="721c2-111">หากระบบพบว่าปริมาณที่เบิกในรายการสินค้าคือ 0 (ศูนย์) คุณไม่สามารถยืนยันการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="721c2-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="721c2-112">ตัวอย่างเช่น ปัญหานี้อาจเกิดขึ้นหากงานถูกยกเลิกและเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่งในรายการสินค้าคือ 100 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="721c2-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="721c2-113">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="721c2-113">Resolution</span></span>

<span data-ttu-id="721c2-114">ตรวจสอบรายการสินค้าของคุณเพื่อให้แน่ใจว่าเปอร์เซ็นต์และปริมาณการจัดส่งน้อยกว่าปริมาณที่สั่งเกินสอดคล้องกับงานที่เบิกสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="721c2-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="721c2-115">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="721c2-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="721c2-116">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="721c2-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="721c2-117">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้าที่เกินกว่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="721c2-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="721c2-118">ปรับปรุงค่าของฟิลด์ **การจัดส่งน้อยกว่าปริมาณที่สั่ง** หรือฟิลด์ **ปริมาณ** ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="721c2-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="721c2-119">ถ้าปัญหายังไม่ได้รับการแก้ไข คุณอาจต้องกรอกฟอร์มงานการเบิกสินค้าเพิ่มเติมให้กับใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องจนกว่าปริมาณที่พร้อมใช้งานจะสอดคล้องกับรายการสินค้าหรือการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="721c2-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
