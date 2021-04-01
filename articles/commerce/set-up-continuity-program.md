---
title: ตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการ
description: บทความนี้อธิบายวิธีการตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการทางโทรศัพท์
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2428cafc45f074f7e2b4c3e59877079b8c1d4a92
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242972"
---
# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="4b35f-103">ตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="4b35f-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b35f-104">บทความนี้อธิบายวิธีการตั้งค่าโปรแกรมความต่อเนื่องสำหรับศูนย์บริการทางโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="4b35f-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="4b35f-105">ในโปรแกรมความต่อเนื่อง ซึ่งเรียกอีกอย่างว่าโปรแกรมใบสั่งที่เกิดซ้ำ ลูกค้าได้รับการจัดส่งผลิตภัณฑ์ปกติตามกำหนดการที่กำหนดไว้ล่วงหน้า </span><span class="sxs-lookup"><span data-stu-id="4b35f-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="4b35f-106">การจัดส่งแต่ละรายการประกอบด้วยผลิตภัณฑ์อื่นด้วยได้ เช่น ในกรณีของสโมสรหนังสือแห่งเดือน หรือผลิตภัณฑ์เดียวกันก็สามารถส่งซ้ำได้</span><span class="sxs-lookup"><span data-stu-id="4b35f-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="4b35f-107">เพื่อตั้งค่าโปรแกรมความต่อเนื่อง คุณต้องดำเนินการต่อไปนี้ให้สำเร็จ</span><span class="sxs-lookup"><span data-stu-id="4b35f-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="4b35f-108">ตั้งค่าพารามิเตอร์ความต่อเนื่องใน **หน้าพารามิเตอร์ศูนย์บริการ**</span><span class="sxs-lookup"><span data-stu-id="4b35f-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="4b35f-109">สร้างโปรแกรมความต่อเนื่องซึ่งระบุรายละเอียด เช่น กำหนดการชำระเงิน ช่วงเวลาของการจัดส่ง และระบุว่ามีการเรียกเก็บเงินล่วงหน้าหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4b35f-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="4b35f-110">คุณต้องเพิ่มรายการผลิตภัณฑ์ที่รวมอยู่ในโปรแกรมความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="4b35f-111">ผลิตภัณฑ์แต่ละรายการได้รับหมายเลขรหัสเหตุการณ์ที่ถูกกำหนดให้ตามลำดับ ซึ่งเริ่มต้นด้วย 1</span><span class="sxs-lookup"><span data-stu-id="4b35f-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="4b35f-112">รหัสเหตุการณ์กำหนดใบสั่งที่ผลิตภัณฑ์ถูกส่ง</span><span class="sxs-lookup"><span data-stu-id="4b35f-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="4b35f-113">ถ้าลูกค้าได้รับผลิตภัณฑ์อื่นในแต่ละการจัดส่ง ผลิตภัณฑ์จะถูกส่งตามลำดับการสั่ง ซึ่งขึ้นอยู่กับรหัสเหตุการณ์ของพวกเขา และเริ่มต้นด้วยเหตุการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4b35f-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="4b35f-114">ถ้าลูกค้าได้รับผลิตภัณฑ์เดียวกันในแต่ละการจัดส่ง รายการประกอบด้วยสินค้าเพียงรายการเดียวที่มีรหัสเหตุการณ์เดียวเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4b35f-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="4b35f-115">เหตุการณ์เดียวกันที่เกิดขึ้นซ้ำ ๆ</span><span class="sxs-lookup"><span data-stu-id="4b35f-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="4b35f-116">คุณสามารถระบุจำนวนครั้งที่มีการเกิดซ้ำของแต่ละเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="4b35f-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="4b35f-117">สร้างผลิตภัณฑ์หลักที่แสดงถึงโปรแกรมความต่อเนื่องที่คุณสร้างไว้ในงาน 2</span><span class="sxs-lookup"><span data-stu-id="4b35f-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="4b35f-118">ถ้าคุณเพิ่มผลิตภัณฑ์นี้ไปยังใบสั่งขาย หน้า **ความต่อเนื่อง** เปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="4b35f-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="4b35f-119">จากนั้นคุณสามารถใช้หน้านั้นเพื่อสร้างใบสั่งจริงอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="4b35f-120">ผลิตภัณฑ์หลักจะไม่ระบุผลิตภัณฑ์แต่ละรายการที่ลูกค้าจะได้รับในการจัดส่งแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="4b35f-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="4b35f-121">หลังจากที่คุณได้ติดตั้งโปรแกรมความต่อเนื่องตามที่อธิบายไว้ข้างต้น คุณสามารถสร้างใบสั่งต่อเนื่องสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4b35f-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="4b35f-122">คุณอาจจะต้องดำเนินการงานการบำรุงรักษาเพิ่มเติมดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4b35f-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="4b35f-123">**อัพเดตรอบระยะเวลาของช่วงเหตุการณ์ต่อเนื่องปัจจุบัน** – ตั้งค่าชุดงานที่จะแจ้งให้ระบบทราบว่ารอบอะไรคือช่วงระยะเวลาของเหตุการณ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4b35f-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="4b35f-124">**สร้างใบสั่งรองที่มีความต่อเนื่อง1** – สร้างใบสั่งรองจากใบสั่งหลักต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="4b35f-125">**ดำเนินการการชำระเงินแบบต่อเนื่อง** – ดำเนินการการเรียกเก็บเงินและการแจ้งเตือนสำหรับการชำระเงินที่เกี่ยวข้องกับใบสั่งขายต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="4b35f-126">**ขยายรายการที่ต่อเนื่อง** (ถ้าจำเป็น) – ขยายจำนวนครั้งของเหตุการณ์ที่ความต่อเนื่องนี้สามารถทำซ้ำ</span><span class="sxs-lookup"><span data-stu-id="4b35f-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="4b35f-127">การทำซ้ำการจัดส่งสามารถขยายเกินข้อจำกัดที่ได้ตั้งค่าไว้ใน **ฟิลด์ความต่อเนื่องขีดจำกัดซ้ำ** ในพารามิเตอร์ศูนย์บริการได้</span><span class="sxs-lookup"><span data-stu-id="4b35f-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="4b35f-128">**ดำเนินการอัพเดตความต่อเนื่อง** (ถ้าจำเป็น) – ซิงโครไนส์การเปลี่ยนแปลงระหว่างโปรแกรมความต่อเนื่องกับใบสั่งขายหลักต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="4b35f-129">**ปิดรายการและใบสั่งหลักที่มีความต่อเนื่อง** – ปิดใบสั่งที่มีความต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="4b35f-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]