---
title: เปลี่ยนโหมดการจัดส่งใน POS
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกและใช้การดำเนินงานโหมดการเปลี่ยนแปลงการจัดส่งใน POS
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965438"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="5a46a-103">เปลี่ยนโหมดการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="5a46a-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a46a-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าและใช้ฟังก์ชัน "เปลี่ยนโหมดการจัดส่ง" ในสภาพแวดล้อมการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="5a46a-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="5a46a-105">ใน Dynamics 365 Commerce รุ่น10.0.10 และรุ่นที่ใหม่กว่า การดำเนินการ **เปลี่ยนโหมดการจัดส่ง** (647) จะพร้อมใช้งานในการเพิ่มไปยังโครงร่างหน้าจอ POS ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5a46a-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="5a46a-106">คุณลักษณะของโหมดการเปลี่ยนแปลงในการจัดส่งช่วยให้คุณมีตัวเลือกในการเปลี่ยนโหมดการจัดส่งสำหรับรายการขายที่ตั้งค่าคอนฟิกการจัดส่งอย่างน้อยหนึ่งรายการบนธุรกรรม POS</span><span class="sxs-lookup"><span data-stu-id="5a46a-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="5a46a-107">ในรุ่นก่อนหน้าของ Commerce คุณต้องไปที่การตั้งค่าคอนฟิกขั้นตอน **จัดส่งทั้งหมด** หรือ **จัดส่งรายการที่เลือก** ทั้งหมด ถ้าคุณต้องการเปลี่ยนโหมดการจัดส่งในรายการที่มีอยู่ซึ่งถูกตั้งค่าคอนฟิกสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="5a46a-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="5a46a-108">กระบวนการนี้ใช้เวลานานและอาจส่งผลให้เกิดการเปลี่ยนแปลงที่เกิดขึ้นโดยไม่ได้ตั้งใจกับจุดเริ่มต้นของการจัดส่งหรือวันที่จัดส่งสำหรับรายการ</span><span class="sxs-lookup"><span data-stu-id="5a46a-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="5a46a-109">ฟังก์ชันใหม่นี้แสดงวิธีการสำรองสำหรับการอัพเดตโหมดการจัดส่งในรายการขายเหล่านี้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="5a46a-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="5a46a-110">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเพิ่มการดำเนินงานไปยังปุ่มบนกริดปุ่ม POS ของคุณ ให้ดูที่ [โครงร่างหน้าจอสำหรับการขายหน้าร้าน](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts)</span><span class="sxs-lookup"><span data-stu-id="5a46a-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="5a46a-111">หลังจากที่มีการตั้งค่าคอนฟิกคุณลักษณะนี้ใน POS เมื่อคุณเลือก **เปลี่ยนโหมดการจัดส่ง** คุณจะได้รับการนำเสนอด้วยหน้ารายการซึ่งช่วยให้คุณสามารถเลือกรายการของธุรกรรมที่คุณต้องการเปลี่ยนโหมดการจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="5a46a-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="5a46a-112">คุณสามารถเลือกบางส่วนหรือทั้งหมดของรายการ หรือจบการทำงานได้โดยไม่ต้องทำการเปลี่ยนแปลงใดๆ</span><span class="sxs-lookup"><span data-stu-id="5a46a-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="5a46a-113">รายการขายที่ได้รับการตั้งค่าคอนฟิกก่อนหน้านี้สำหรับการจัดส่งเป็นรายการเดียวในรายการที่คุณสามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="5a46a-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="5a46a-114">ถ้าคุณต้องการเปลี่ยนแปลงรายการที่กำหนดสำหรับการเบิกสินค้าหรือการจัดส่งสินค้า คุณต้องใช้การดำเนินการ **จัดส่งทั้งหมด** หรือ **จัดส่งรายการที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="5a46a-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="5a46a-115">ในทางตรงกันข้าม ถ้าคุณต้องการเปลี่ยนแปลงรายการที่กำหนดเป็นการจัดส่งไปยังการเบิกสินค้าหรือการจัดส่งสินค้า คุณต้องใช้การดำเนินการ  **เบิกสินค้าทั้งหมด** **เบิกสินค้าที่เลือก** หรือ **จัดส่งทั้งหมด** หรือ **จัดส่งที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="5a46a-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="5a46a-116">หลังจากที่คุณเลือกรายการที่คุณต้องการเปลี่ยนแปลง ให้คลิก **เปลี่ยนโหมดการจัดส่ง** ที่จะได้รับการแจ้งเตือนเพื่อเลือกตัวเลือกโหมดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="5a46a-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="5a46a-117">ถ้าคุณได้เลือกหลายรายการเพื่อเปลี่ยนแปลง POS จะแสดงเฉพาะโหมดการจัดส่งที่ได้รับการตั้งค่าคอนฟิกเป็นยอมรับได้สำหรับผลิตภัณฑ์ทั้งหมดที่เลือกไว้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5a46a-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="5a46a-118">สามารถตั้งค่าคอนฟิกโหมดการจัดส่งเพื่อสนับสนุนผลิตภัณฑ์และที่อยู่ในการจัดส่งที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="5a46a-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="5a46a-119">ถ้ามีโหมดการจัดส่งที่ได้รับการยอมรับสำหรับชุดผลิตภัณฑ์และที่อยู่หนึ่งรายการ แต่ไม่ได้รับการยอมรับสำหรับชุดผลิตภัณฑ์และที่อยู่อื่นที่เลือกไว้ โหมดการจัดส่งจะไม่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="5a46a-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="5a46a-120">คุณอาจจำเป็นต้องเลือกรายการทีละรายการและเปลี่ยนโหมดการจัดส่งสำหรับแต่ละรายการโดยแยกกัน ถ้าคุณต้องการเลือกโหมดการจัดส่งสำหรับผลิตภัณฑ์หนึ่งที่ไม่ได้รับการสนับสนุนโดยผลิตภัณฑ์อื่น</span><span class="sxs-lookup"><span data-stu-id="5a46a-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="5a46a-121">หลังจากที่คุณเลือกโหมดการจัดส่งใหม่ หน้าธุรกรรมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="5a46a-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="5a46a-122">เมื่อต้องการตรวจสอบการเลือกโหมดการจัดส่งใหม่ของคุณ ให้เลือกแท็บ **การจัดส่ง** ในรายการธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="5a46a-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a46a-123">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5a46a-123">Additional resources</span></span>

[<span data-ttu-id="5a46a-124">สร้างใบสั่งของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="5a46a-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="5a46a-125">กำหนดอีเมลของธุรกรรมตามวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="5a46a-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
