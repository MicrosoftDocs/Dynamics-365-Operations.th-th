--- 
title: "ตั้งค่าคอนฟิกระบบในการส่งอีเมลที่เกี่ยวข้องกับลำดับงานไปยังผู้ใช้"
description: "คุณสามารถตั้งค่าคอนฟิกระบบเพื่อส่งข้อความอีเมลไปยังผู้ใช้เมื่อเกิดเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="68538-103">ตั้งค่าคอนฟิกระบบในการส่งอีเมลที่เกี่ยวข้องกับลำดับงานไปยังผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="68538-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68538-104">คุณสามารถตั้งค่าคอนฟิกระบบเพื่อส่งข้อความอีเมลไปยังผู้ใช้เมื่อเกิดเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="68538-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="68538-105">ตัวอย่างเช่น สามารถส่งข้อความอีเมลให้กับผู้ใช้เมื่อเอกสารถูกกำหนดให้กับผู้ใช้เหล่านั้นเพื่อการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="68538-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="68538-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="68538-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="68538-107">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="68538-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="68538-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="68538-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="68538-109">คลิกตัวเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="68538-109">Click User options.</span></span>
4. <span data-ttu-id="68538-110">คลิกแท็บลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="68538-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="68538-111">ตรวจสอบให้แน่ใจว่ามีการขยายส่วน การแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="68538-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="68538-112">ในส่วน การแจ้งเตือน คุณสามารถระบุวิธีที่คุณต้องการให้ผู้ใช้รับการแจ้งเตือนเกี่ยวกับเหตุการณ์ที่เกี่ยวข้องกับลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="68538-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="68538-113">ในฟิลด์ชนิดการแจ้งเตือนของลำดับงานของสินค้าในรายการ เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="68538-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="68538-114">แบบกลุ่ม – การแจ้งเตือนสำหรับสินค้าในรายการจะถูกจัดกลุ่มลงในข้อความอีเมลเดียว</span><span class="sxs-lookup"><span data-stu-id="68538-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="68538-115">แบบเดี่ยว – ข้อความอีเมลที่ถูกส่งสำหรับสินค้าในรายการแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="68538-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="68538-116">ถ้าคุณต้องการให้ผู้ใช้สามารถได้รับการแจ้งเตือนในไคลเอนต์ เลือกกล่องกาเครื่องหมาย ส่งการแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="68538-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="68538-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="68538-117">Click Save.</span></span>
7. <span data-ttu-id="68538-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="68538-118">Close the page.</span></span>


