---
title: ตั้งค่าพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์
description: หัวข้อนี้อธิบายวิธีการตั้งค่า Microsoft Dynamics 365 Supply Chain Management และแอป Finance and Operations บนมือถือ (Dynamics 365) เพื่อรันพื้นที่ทำงานการจัดการสินทรัพย์บนมือถือ ซึ่งผู้ปฏิบัติงานสามารถใช้เพื่อปฏิบัติงานการจัดการสินทรัพย์
author: johanhoffmann
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9c2410c50b5d289792e2cc364674e1e093653590
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033233"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="4577f-103">ตั้งค่าพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4577f-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4577f-104">หัวข้อนี้อธิบายวิธีการตั้งค่า Microsoft Dynamics 365 Supply Chain Management และแอป Finance and Operations บนมือถือ (Dynamics 365) เพื่อรันพื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือ ซึ่งผู้ปฏิบัติงานสามารถใช้เพื่อปฏิบัติงานการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4577f-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="4577f-105">ตั้งค่าผู้ใช้เจ้าหน้าที่บำรุงรักษาใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4577f-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="4577f-106">สำหรับผู้ใช้แต่ละคนที่ต้องใช้พื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4577f-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="4577f-107">ใน Supply Chain Management ไปที่ **ทรัพยากรบุคคล \> ผู้ปฏิบัติงาน** ให้แน่ใจว่ามีเรกคอร์ดผู้ปฏิบัติงานให้กับผู้ใช้ที่คุณต้องการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="4577f-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="4577f-108">สร้างเรกคอร์ดผู้ปฏิบัติงานใหม่ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4577f-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="4577f-109">ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> ผู้ปฏิบัติงาน \> ผู้ปฏิบัติงาน** และตรวจสอบให้แน่ใจว่าเรกคอร์ดผู้ปฏิบัติงานที่คุณระบุ (หรือสร้างขึ้น) ในขั้นตอนก่อนหน้านี้ถูกแม็ปไปเรกคอร์ดเจ้าหน้าที่บำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4577f-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="4577f-110">สร้างเรกคอร์ดเจ้าหน้าที่บำรุงรักษาใหม่ตามที่ต้องการ และตั้งค่าฟิลด์ **ผู้ปฏิบัติงาน** เป็นเรกคอร์ดผู้ปฏิบัติงานจากขั้นตอนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="4577f-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="4577f-111">ไปที่ **การจัดการสินทรัพย์ \> การตั้งค่า \> ผู้ปฏิบัติงาน \> กลุ่มเจ้าหน้าที่บำรุงรักษา** และตรวจสอบให้แน่ใจว่าเรกคอร์ดเจ้าหน้าที่บำรุงรักษาที่คุณระบุ (หรือสร้างขึ้น) ในขั้นตอนก่อนหน้านี้อยู่ในกลุ่มเจ้าหน้าที่บำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4577f-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="4577f-112">ไปที่ **การจัดการระบบ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="4577f-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="4577f-113">เลือกผู้ใช้ที่เกี่ยวข้องในตารางกริด</span><span class="sxs-lookup"><span data-stu-id="4577f-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="4577f-114">บนแท็บ **รายละเอียดผู้ใช้** ให้ตั้งค่าฟิลด์ **บุคคล** เป็นบัญชีผู้ปฏิบัติงานที่คุณต้องการเชื่อมโยงกับบัญชีผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4577f-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="4577f-115">บัญชีผู้ปฏิบัติงานนี้ควรเป็นเรกคอร์ดผู้ปฏิบัติงานที่คุณระบุ (หรือสร้างขึ้น) ในขั้นตอนที่ 1 และแม็ปกับเรกคอร์ดเจ้าหน้าที่บำรุงรักษาในขั้นตอนที่ 2</span><span class="sxs-lookup"><span data-stu-id="4577f-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="4577f-116">สิทธิการได้รับอนุญาตของผู้ใช้และบทบาทความปลอดภัยจะใช้กับคุณลักษณะของพื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือเช่นเดียวกับที่ใช้กับคุณลักษณะของอินเทอร์เฟสผู้ใช้ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4577f-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="4577f-117">ดังนั้น ผู้ใช้ทุกคนที่คุณตั้งค่าให้เข้าถึงพื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือต้องมีบทบาทความปลอดภัยที่จำเป็นเพื่อดำเนินการงานที่คล้ายกันโดยตรงใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="4577f-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="4577f-118">เผยแพร่พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4577f-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="4577f-119">เมื่อต้องการให้คุณลักษณะการจัดการสินทรัพย์พร้อมใช้งานในแอป Finance and Operations บนมือถือ (Dynamics 365) คุณต้องเผยแพร่พื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือ</span><span class="sxs-lookup"><span data-stu-id="4577f-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="4577f-120">ใน Supply Chain Management ให้เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์ในมุมด้านขวาบน) แล้วเลือก **แอปบนมือถือ** ในเมนู</span><span class="sxs-lookup"><span data-stu-id="4577f-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="4577f-121">ในกล่องโต้ตอบ **จัดการแอปบนมือถือ** ให้ค้นหาไทล์ **การจัดการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="4577f-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="4577f-122">ถ้ามีข้อความ "ในข้อมูลเมตา - ไม่ได้เผยแพร่" พื้นที่ทำงานนี้ไม่ได้รับการเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="4577f-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="4577f-123">ถ้ามีข้อความ "ในข้อมูลเมตา - เผยแพร่แล้ว" พื้นที่ทำงานนี้เผยแพร่แล้ว และคุณสามารถข้ามส่วนที่เหลือของกระบวนงานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="4577f-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="4577f-124">![จัดการกล่องโต้ตอบแอปบนมือถือ](media/mobile-workspaces.png "จัดการกล่องโต้ตอบแอปบนมือถือ")</span><span class="sxs-lookup"><span data-stu-id="4577f-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="4577f-125">เลือกไทล์ **การจัดการสินทรัพย์** แล้วเลือก **เผยแพร่** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="4577f-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="4577f-126">หลังจากเวลาผ่านไปสองสามวินาที คุณควรได้รับการแจ้งเตือนที่ระบุว่าพื้นที่ทำงานได้รับการเผยแพร่เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="4577f-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="4577f-127">นอกจากนี้ ข้อความบนไทล์ควรเปลี่ยนเป็น "ในข้อมูลเมตา - เผยแพร่แล้ว"</span><span class="sxs-lookup"><span data-stu-id="4577f-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="4577f-128">ติดตั้งและตั้งค่าแอป Finance and Operations บนมือถือ (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="4577f-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="4577f-129">ไปที่หนึ่งในร้านค้าแอปต่อไปนี้เพื่อติดตั้งแอป **Microsoft Finance and Operations (Dynamics 365)** บนอุปกรณ์เคลื่อนที่ของคุณ:</span><span class="sxs-lookup"><span data-stu-id="4577f-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="4577f-130">สำหรับอุปกรณ์ Google Android</span><span class="sxs-lookup"><span data-stu-id="4577f-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="4577f-131">สำหรับอุปกรณ์ Apple iOS</span><span class="sxs-lookup"><span data-stu-id="4577f-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="4577f-132">เปิดแอป Finance and Operations (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="4577f-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="4577f-133">หน้าการลงชื่อเข้าใช้ควรปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4577f-133">The sign-in page should appear.</span></span> <span data-ttu-id="4577f-134">ในฟิลด์ **ลงชื่อเข้าใช้** ป้อน URL Supply Chain Management ของคุณ หรือเลือก URL ล่าสุดในรายการ **รายการสภาพแวดล้อมล่าสุด** แล้วแตะ **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="4577f-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="4577f-135">![หน้าลงชื่อเข้าใช้](media/mobile-app-sign-in.png "หน้าลงชื่อเข้าใช้")</span><span class="sxs-lookup"><span data-stu-id="4577f-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="4577f-136">หากคุณได้รับการเตือนให้ยืนยันการเชื่อมต่อ ให้เลือกกล่องกาเครื่องหมาย **ฉันเข้าใจ** แล้วแตะ **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="4577f-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="4577f-137">บนหน้า **เลือกบัญชี** ให้ใช้บัญชี Microsoft ของคุณเพื่อเข้าสู่ระบบแอปสำหรับอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="4577f-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="4577f-138">หน้า **พื้นที่ทำงาน** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="4577f-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="4577f-139">โดยจะแสดงรายการพื้นที่ทำงานบนมือถือทุกพื้นที่ที่ได้รับการเผยแพร่โดยอินสแตนซ์ Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="4577f-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="4577f-140">![รายการของพื้นที่ทำงาน](media/mobile-app-workspaces.png "รายการของพื้นที่ทำงาน")</span><span class="sxs-lookup"><span data-stu-id="4577f-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="4577f-141">ถ้าคุณต้องเปลี่ยนนิติบุคคล (บริษัท) แตะปุ่มเมนู (บางครั้งอาจเรียกว่า แฮมเบอร์เกอร์ หรือปุ่มแฮมเบอร์เกอร์) ในมุมซ้ายบน แล้วแตะปุ่ม **เปลี่ยนบริษัท**</span><span class="sxs-lookup"><span data-stu-id="4577f-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="4577f-142">![การเปลี่ยนแปลงนิติบุคคล](media/mobile-app-change-comp.png "การเปลี่ยนแปลงนิติบุคคล")</span><span class="sxs-lookup"><span data-stu-id="4577f-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="4577f-143">บนหน้า **พื้นที่ทำงาน** ให้เลือกพื้นที่ทำงานที่คุณต้องการใช้งานเพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="4577f-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="4577f-144">![พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์](media/mobile-app-asset-workspace.png "พื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์")</span><span class="sxs-lookup"><span data-stu-id="4577f-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="4577f-145">ทำงานบนพื้นที่ทำงานบนอุปกรณ์เคลื่อนที่สำหรับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4577f-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="4577f-146">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีใช้งานพื้นที่ทำงาน **การจัดการสินทรัพย์** บนมือถือ โปรดดูที่ [ใช้งานพื้นที่ทำงานการจัดการสินทรัพย์บนมือถือ](asset-management-mobile-workspace.md)</span><span class="sxs-lookup"><span data-stu-id="4577f-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="4577f-147">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับแอป Finance and Operations บนมือถือ (Dynamics 365) โปรดดูที่ [หน้าแรกของแอปบนมือถือ](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md)</span><span class="sxs-lookup"><span data-stu-id="4577f-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>
