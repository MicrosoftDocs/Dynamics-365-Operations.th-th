---
title: การทำเครื่องหมายสินค้าคงคลังด้วยการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับตัวเลือกที่พร้อมใช้งานสำหรับการทำเครื่องหมายสินค้าคงคลังในใบสั่งที่ยืนยันแล้วเมื่อคุณใช้การเพิ่มประสิทธิภาพของการวางแผน
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7813f570afb0260e6740507c9504320c3e87be93
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263361"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="f9f1b-103">การทำเครื่องหมายสินค้าคงคลังด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="f9f1b-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9f1b-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับตัวเลือกที่พร้อมใช้งานสำหรับการทำเครื่องหมายสินค้าคงคลังในใบสั่งที่ยืนยันแล้วเมื่อคุณใช้การเพิ่มประสิทธิภาพของการวางแผน</span><span class="sxs-lookup"><span data-stu-id="f9f1b-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="f9f1b-105">*การทำเครื่องหมาย* ใช้เพื่อลิงค์การจัดหาวัสดุและความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="f9f1b-106">จะเหมือนกับ *การเชื่อมโยงความต้องการกับการจัดซื้อ* ซึ่งบ่งชี้ว่าการวางแผนหลักคาดว่าจะครอบคลุมความต้องการอย่างไร</span><span class="sxs-lookup"><span data-stu-id="f9f1b-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="f9f1b-107">จากมุมมองการวางแผน ความแตกต่างที่สำคัญคือการทำเครื่องหมายที่มีการทำเครื่องหมายเป็นแบบถาวรมากกว่าการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="f9f1b-108">การทำเครื่องหมายถูกนำมาใช้เพื่อสนับสนุนสถานการณ์การคิดต้นทุนพิเศษสำหรับเข้าก่อนออกก่อน (FIFO) และเข้าหลังออกก่อน (LIFO)</span><span class="sxs-lookup"><span data-stu-id="f9f1b-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="f9f1b-109">อย่างไรก็ตาม ขณะนี้ยังใช้สำหรับสถานการณ์ที่ไม่ใช่การคิดต้นทุนบางอย่างด้วย</span><span class="sxs-lookup"><span data-stu-id="f9f1b-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="f9f1b-110">การทำเครื่องหมายระหว่างการจัดหาวัสดุและความต้องการเป็นตัวเลือกและเกือบถาวร</span><span class="sxs-lookup"><span data-stu-id="f9f1b-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="f9f1b-111">การทำเครื่องหมายอาจถูกลบออกด้วยตนเองโดยผู้ใช้ หรือสามารถลบออกได้โดยการรันการกระจายบรรทัดใบสั่งขายที่มีการเลือกตัวเลือก **ลบการทำเครื่องหมาย**</span><span class="sxs-lookup"><span data-stu-id="f9f1b-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="f9f1b-112">การเชื่อมโยงความต้องการกับการจัดซื้อมีการควบคุมโดยการวางแผนหลักในระหว่างความครอบคลุมเพื่อเชื่อมโยงความต้องการกับการจัดหาวัสดุที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f9f1b-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="f9f1b-113">การเชื่อมโยงความต้องการกับการจัดซื้อสามารถอัพเดตสำหรับแต่ละการวางแผนรันเพื่อเพิ่มประสิทธิภาพการจัดหาวัสดุที่จำเป็นสำหรับการครอบคลุมความต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="f9f1b-114">เมื่อการวางแผนหลักอัพเดตข้อมูลการเชื่อมโยงความต้องการกับการจัดซื้อดังกล่าว จะทำให้เกิดการทำเครื่องหมายใดๆที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="f9f1b-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="f9f1b-115">การเชื่อมโยงความต้องการกับการจัดซื้อจะเริ่มต้นโดยรวมถึงการทำเครื่องหมายที่เกี่ยวข้อง การจองสินค้าคงคลังคงเหลือ และการจองสินค้าตามใบสั่ง ตามลำดับต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f9f1b-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="f9f1b-116">การทำเครื่องหมายระหว่างความต้องการและอุปทาน</span><span class="sxs-lookup"><span data-stu-id="f9f1b-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="f9f1b-117">การจองปริมาณคงคลังคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-117">On-hand reservations</span></span>
1. <span data-ttu-id="f9f1b-118">การจองตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="f9f1b-118">On-order reservations</span></span>

<span data-ttu-id="f9f1b-119">เมื่อคุณยืนยันแผนการใบสั่ง กล่องโต้ตอบ **การยืนยัน** จะแสดงฟิลด์ **การทำเครื่องหมายการอัพเดต** ที่คุณใช้เพื่อตั้งค่าตัวเลือกการทำเครื่องหมายสำหรับใบสั่งที่สร้างขึ้นในระหว่างการยืนยันยอด</span><span class="sxs-lookup"><span data-stu-id="f9f1b-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="f9f1b-120">เลือกค่าใดค่าหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f9f1b-120">Select one of the following values:</span></span>

- <span data-ttu-id="f9f1b-121">**ไม่** – ไม่มีการทำเครื่องหมายสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="f9f1b-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="f9f1b-122">**มาตรฐาน** – อัพเดตการทำเครื่องหมายสินค้าคงคลังตามการเชื่อมโยงความต้องการกับการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="f9f1b-123">มีการทำเครื่องหมายใบสั่งความต้องการ (อุปสงค์) ตามใบสั่งการเติมสินค้า (อุปทาน)</span><span class="sxs-lookup"><span data-stu-id="f9f1b-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="f9f1b-124">ถ้าปริมาณบางปริมาณยังคงอยู่ในใบสั่งการเติมสินค้า จะไม่มีการทำเครื่องหมาย และข้อมูลอ้างอิงจะถูกปล่อยว่างไว้</span><span class="sxs-lookup"><span data-stu-id="f9f1b-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="f9f1b-125">ตัวอย่างเช่น ถ้าใบสั่งขายสำหรับ 100 ea ถูกโยงกับใบสั่งซื้อสำหรับ 150 ea จะมีการกำหนดข้อมูลอ้างอิงให้กับใบสั่งขายเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f9f1b-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="f9f1b-126">**ขยาย** – ทำเครื่องหมายทั้งใบสั่งความต้องการ (อุปสงค์) และใบสั่งการเติมสินค้า (อุปทาน) โดยไม่คำนึงว่ายังคงมีปริมาณอยู่บนใบสั่งการเติมสินค้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f9f1b-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="f9f1b-127">ตัวอย่างเช่น ถ้าใบสั่งขายสำหรับ 100 ea ถูกโยงกับใบสั่งซื้อสำหรับ 150 ea จะมีการกำหนดข้อมูลอ้างอิงให้กับทั้งใบสั่งขายและใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="f9f1b-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]