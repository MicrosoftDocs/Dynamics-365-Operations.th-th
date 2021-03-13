---
title: เรียกคืนการดำเนินงานใบสั่งใน POS
description: หัวข้อนี้อธิบายความสามารถของลักษณะการทำงานที่พร้อมใช้งานสำหรับหน้าการเรียกคืนใบสั่งที่ปรับปรุงใน POS
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010085"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="819bd-103">เรียกคืนการดำเนินงานใบสั่งใน POS</span><span class="sxs-lookup"><span data-stu-id="819bd-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="819bd-104">การดำเนินงาน **เรียกคืนใบสั่ง** ในการขายหน้าร้าน (POS) ของ Commerce ให้คุณลักษณะการค้นหาใบสั่งที่มีการอัปเดตและการกรองข้อมูล และข้อมูลเฉพาะใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="819bd-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="819bd-105">คุณลักษณะนี้พร้อมใช้งานใน Commerce รุ่น 10.0.15 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="819bd-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="819bd-106">เมื่อต้องการเปิดใช้งานฟังก์ชันนี้ ให้เปิดลักษณะการทำงาน **การดำเนินงานเรียกคืนใบสั่งที่ดีขึ้นใน POS** ในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="819bd-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="819bd-107">หลังจากที่คุณเปิดใช้งานลักษณะการทำงานแล้ว ให้พิจารณาการอัปเดต [เค้าโครงหน้าจอของคุณ](pos-screen-layouts.md) ใน POS เพื่อใช้ประโยชน์จากความสามารถในการเปลี่ยนแปลงบางอย่าง</span><span class="sxs-lookup"><span data-stu-id="819bd-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="819bd-108">การตั้งค่าคอนฟิกของปุ่มการดำเนินงาน **เรียกคืนใบสั่ง** ช่วยให้องค์กรสามารถจัดวางการดำเนินงานด้วยการแสดงผลที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="819bd-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![การตั้งค่าคอนฟิกกริดปุ่ม](media/recallorderbuttongrid.png)

<span data-ttu-id="819bd-110">ตัวเลือกการแสดงมีดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="819bd-110">The display options are as follows.</span></span>
- <span data-ttu-id="819bd-111">**ไม่มี** - ตัวเลือกนี้จะใช้การดำเนินงานที่ไม่มีการแสดงผลที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="819bd-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="819bd-112">เมื่อผู้ใช้เปิดการดำเนินงานที่มีการตั้งค่าคอนฟิกนี้ ผู้ใช้จะได้รับการแจ้งเตือนให้ค้นหา และค้นหาใบสั่ง หรือเลือกจากตัวกรองใบสั่งที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="819bd-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="819bd-113">**ใบสั่งเพื่อตอบสนอง** – เมื่อผู้ใช้เปิดใช้งานการดำเนินการ การสอบถามจะรันโดยอัตโนมัติ เพื่อค้นหาและแสดงรายการของใบสั่งที่จะเติมสินค้าโดยร้านค้า</span><span class="sxs-lookup"><span data-stu-id="819bd-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="819bd-114">ใบสั่งเหล่านี้ได้รับการตั้งค่าคอนฟิกสำหรับการเบิกสินค้าในร้านค้าหรือการจัดส่งสินค้าในร้านค้า และรายการของใบสั่งเหล่านี้ยังไม่ได้รับการเบิกสินค้าหรือบรรจุ</span><span class="sxs-lookup"><span data-stu-id="819bd-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="819bd-115">**ใบสั่งเพื่อเบิกสินค้า** – เมื่อผู้ใช้เปิดใช้งานการดำเนินการ การสอบถามจะรันโดยอัตโนมัติ เพื่อค้นหาและแสดงรายการของใบสั่งที่จะตั้งค่าคอนฟิกไว้สำหรับการเบิกสินค้าในร้านค้าที่ร้านค้าปัจจุบันของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="819bd-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="819bd-116">**ใบสั่งเพื่อจัดส่งสินค้า** – เมื่อผู้ใช้เปิดใช้งานการดำเนินการ การสอบถามจะรันโดยอัตโนมัติ เพื่อค้นหาและแสดงรายการของใบสั่งที่จะตั้งค่าคอนฟิกไว้สำหรับการจัดส่งสินค้าที่ร้านค้าปัจจุบันของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="819bd-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="819bd-117">เมื่อเรียกใช้การดำเนินงาน **เรียกคืนใบสั่ง** จาก POS ถ้ามีการตั้งค่าคอนฟิกการแสดงผลเป็น **ไม่มี** ผู้ใช้จะสามารถค้นหา และดึงข้อมูลใบสั่งได้วิธีใดวิธีหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="819bd-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="819bd-118">สแกนบาร์โค้ดของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="819bd-118">Scan order barcodes.</span></span> <span data-ttu-id="819bd-119">การทำเช่นนี้จะค้นหาหมายเลขใบสั่ง การอ้างอิงช่องทาง และฟิลด์รหัสการรับสินค้าสำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="819bd-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="819bd-120">เลือกไอคอน **ค้นหาใบสั่ง** หรือ **ค้นหาและตัวกรอง** บน AppBar เพื่อใช้กลไกการกรองข้อมูลเพื่อค้นหาใบสั่งที่ตรงกับเงื่อนไขของตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="819bd-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="819bd-121">เลือกจากตัวกรองที่กำหนดไว้ล่วงหน้าจากเมนูแบบหล่นลงของ **แสดงใบสั่ง** (ใบสั่งที่จะตอบสนอง ใบสั่งที่จะเบิกสินค้า หรือใบสั่งที่จะจัดส่ง)</span><span class="sxs-lookup"><span data-stu-id="819bd-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="819bd-123">หลังจากที่มีการใช้เงื่อนไขการค้นหา โปรแกรมประยุกต์จะแสดงรายการของใบสั่งขายที่ตรงกัน</span><span class="sxs-lookup"><span data-stu-id="819bd-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="819bd-125">ผู้ใช้สามารถเลือกใบสั่งในรายการเพื่อดูรายละเอียดเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="819bd-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="819bd-126">แผงข้อมูลทางด้านขวาของหน้าจอจะแสดงข้อมูลจำเพาะเกี่ยวกับใบสั่งที่เลือก รวมถึงรายละเอียดของรายการใบสั่ง รายละเอียดการจัดส่ง และรายละเอียดการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="819bd-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="819bd-127">จาก AppBar ผู้ใช้สามารถเลือกการดำเนินงานได้</span><span class="sxs-lookup"><span data-stu-id="819bd-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="819bd-128">ขึ้นอยู่กับสถานะของใบสั่ง การดำเนินงานบางอย่างอาจไม่ได้รับการเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="819bd-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="819bd-129">**ส่งคืน** – ดำเนินการส่งคืนสำหรับใบแจ้งหนี้หนึ่งใบขึ้นไปที่เกี่ยวข้องกับใบสั่งของลูกค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="819bd-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="819bd-130">**ยกเลิก** – ออกการยกเลิกแบบเต็มของใบสั่งขายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="819bd-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="819bd-131">**การเติมสินค้า** – โอนย้ายผู้ใช้ไปที่หน้าการเติมสินค้าตามใบสั่ง ซึ่งจะถูกกรองไว้ล่วงหน้าสำหรับใบสั่งที่เลือก</span><span class="sxs-lookup"><span data-stu-id="819bd-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="819bd-132">เฉพาะรายการใบสั่งที่เปิดสำหรับการเติมสินค้าตามร้านค้าของผู้ใช้สำหรับใบสั่งที่เลือกเท่านั้นที่จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="819bd-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="819bd-133">**แก้ไข** – อนุญาตให้ผู้ใช้ทำการเปลี่ยนแปลงใบสั่งของลูกค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="819bd-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="819bd-134">**เบิกสินค้า** – เปิดใช้งานขั้นตอนการเบิกสินค้า ซึ่งช่วยให้ผู้ใช้สามารถเลือกผลิตภัณฑ์ที่จะเบิกสินค้า และสร้างธุรกรรมการเบิกสินค้าสำหรับการขาย</span><span class="sxs-lookup"><span data-stu-id="819bd-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
