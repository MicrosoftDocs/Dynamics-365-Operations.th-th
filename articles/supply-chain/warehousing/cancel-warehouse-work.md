---
title: ยกเลิกงานในคลังสินค้าสำหรับการจัดการข้อยกเว้น
description: หัวข้อนี้จะอธิบายถึงฟังก์ชันยกเลิกการทำงานที่ช่วยให้หัวหน้างานคลังสินค้าจัดการกับงานที่ถูกบล็อค
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205816"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="efb2d-103">ยกเลิกงานในคลังสินค้าสำหรับการจัดการข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="efb2d-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efb2d-104">ฟังก์ชันยกเลิกงานใน Microsoft Dynamics 365 Supply Chain Management ช่วยให้ผู้ดูแลระบบยกเลิกงานคลังสินค้าที่กำลังดำเนินการอยู่ แต่ถูกบล็อกโดยระบบ หรือไม่สามารถทำให้สมบูรณ์ได้เนื่องจากสถานการณ์ยกเว้น</span><span class="sxs-lookup"><span data-stu-id="efb2d-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="efb2d-105">ฟังก์ชันนี้เป็นตัวเลือกที่น่าสนใจและมีความปลอดภัยสำหรับสคริปต์แก้ไข SQL ที่แก้ไขข้อมูลที่ไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="efb2d-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="efb2d-106">อย่างไรก็ตาม ปกติแล้วสคริปต์เหล่านี้มักจะมีการร้องขอโดยผู้เชี่ยวชาญด้านไอที ผู้ใช้ในบริษัทสามารถใช้ฟังก์ชันยกเลิกงานได้หากมีสิทธิ์ของผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="efb2d-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="efb2d-107">คุณสามารถเข้าถึงฟังก์ชันยกเลิกงานได้ที่ **การจัดการคลังสินค้า** \> **งานประจำงวด** \> **ล้างข้อมูล \> ยกเลิกงาน**</span><span class="sxs-lookup"><span data-stu-id="efb2d-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="efb2d-108">ในกล่องโต้ตอบ **ยกเลิกงาน** ให้ระบุรหัสงานของงานที่จะยกเลิก แล้วเลือก**ตกลง**</span><span class="sxs-lookup"><span data-stu-id="efb2d-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="efb2d-109">งานคลังสินค้าที่สามารถยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="efb2d-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="efb2d-110">ระหว่างการดำเนินงานการเบิกสินค้าในคลังสินค้า ผู้ปฏิบัติงานอาจพบสถานการณ์ที่มีการลงทะเบียนปริมาณเป็นเบิกสินค้าจากสถานที่เก็บสินค้าไปยังสถานที่ของผู้ใช้ แต่จะไม่สามารถลงทะเบียนการดำเนินงานการส่งสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="efb2d-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="efb2d-111">สาเหตุที่งานถูกบล็อก มักเป็นเพราะข้อมูลคลังสินค้าไม่สอดคล้องกัน แต่ก็ไม่ใช่เพราะเหตุผลนี้เสมอไป</span><span class="sxs-lookup"><span data-stu-id="efb2d-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="efb2d-112">ซึ่งแตกต่างจากฟังก์ชันยกเลิกปกติที่สามารถเข้าถึงได้โดยใช้ปุ่ม **ยกเลิก** บนหัวข้อของงาน ฟังก์ชันยกเลิกงานไม่จำเป็นต้องมีรายการงานที่เสร็จสมบูรณ์ล่าสุดที่รายการงานของชนิด **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="efb2d-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="efb2d-113">กล่าวคือ สำหรับฟังก์ชันยกเลิกงาน ตรรกะการยกเลิกสามารถเรียกใช้ได้แม้ว่าปริมาณสินค้าของรายการงานเป็นสถานที่ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="efb2d-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="efb2d-114">สำหรับงานที่ต้องยกเลิกเนื่องจากสาเหตุเกี่ยวกับการดำเนินการ ผู้ใช้คลังสินค้าต้องใช้ฟังก์ชันยกเลิกปกติต่อในเพจงาน</span><span class="sxs-lookup"><span data-stu-id="efb2d-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="efb2d-115">เฉพาะงานชนิด **การขาย** **การโอนย้ายการตัดสินค้า** **การเบิกวัตถุดิบ** หรือ **การเติมสินค้า** ที่สามารถยกเลิกได้โดยใช้ฟังก์ชันยกเลิกงาน</span><span class="sxs-lookup"><span data-stu-id="efb2d-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="efb2d-116">ตรรกะการยกเลิกจะไม่มีการเรียกใช้สำหรับงานการเบิกวัตถุดิบที่หยุดใช้งาน หรืองานที่สามารถยกเลิกได้โดยใช้ฟังก์ชันยกเลิกปกติ (ดูหมายเหตุก่อนหน้า)</span><span class="sxs-lookup"><span data-stu-id="efb2d-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="efb2d-117">ในการปลดบล็อกงาน ระบบจะยกเลิกรายการงานที่คงเหลือ และแก้ไขข้อมูลคลังสินค้าที่เชื่อมโยงกับรหัสงานที่ผู้ใช้ระบุ</span><span class="sxs-lookup"><span data-stu-id="efb2d-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="efb2d-118">กระบวนการจัดการคลังสินค้าทั่วไปที่เกี่ยวข้องกับปริมาณสินค้าที่ได้รับผลกระทบสามารถดำเนินการต่อได้</span><span class="sxs-lookup"><span data-stu-id="efb2d-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="efb2d-119">เมื่อต้องการนำสินค้าที่ได้รับผลกระทบในสถานที่เฉพาะหลังจากที่ยกเลิกงานแล้ว ผู้ใช้ต้องใช้การดำเนินการเคลื่อนไหวของสินค้าคงคลัง หรือการปรับปรุงปริมาณบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="efb2d-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>
