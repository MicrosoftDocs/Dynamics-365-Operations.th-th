---
title: สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายว่าใช้งานอยู่
description: หัวข้อนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์ สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) ใน Dynamics 365 for Finance and Operations
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d6df2068f99a42764fc13f282a7c38099109e06
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887098"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="951fb-103">สร้างผู้ให้บริการการตั้งค่าคอนฟิกและทำเครื่องหมายว่าใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="951fb-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="951fb-104">หัวข้อนี้อธิบายวิธีที่ผู้ใช้ที่ถูกกำหนดให้รับบทบาทเป็นผู้ดูแลระบบหรือนักพัฒนาการรายงานอิเล็กทรอนิกส์ สามารถสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับการรายงานอิเล็กทรอนิกส์ (ER) ใน Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="951fb-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER) in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="951fb-105">การตั้งค่าคอนฟิก ER แต่ละครั้ง จะอ้างถึงตัวให้บริการให้เป็นผู้สร้างการตั้งค่าคอนฟิก </span><span class="sxs-lookup"><span data-stu-id="951fb-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="951fb-106">ในตัวอย่างนี้ คุณจะสร้างตัวให้บริการการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง Litware, inc ขั้นตอนเหล่านี้สามารถได้ในบริษัทอื่นใด ในฐานะตัวให้บริการการตั้งค่าคอนฟิก ER ที่ใช้ร่วมกันระหว่างบริษัททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="951fb-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="951fb-107">สร้างผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="951fb-107">Create a provider</span></span>
1. <span data-ttu-id="951fb-108">ไปที่ **บานหน้าต่างนำทาง** ในมุมบนซ้าย และเลือก **การจัดการองค์กร**</span><span class="sxs-lookup"><span data-stu-id="951fb-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="951fb-109">ไปที่ **พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="951fb-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="951fb-110">ไปที่ **ลิงค์ที่เกี่ยวข้อง > ตัวให้บริการการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="951fb-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="951fb-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="951fb-111">Select **New**.</span></span>
    - <span data-ttu-id="951fb-112">เรกคอร์ดของผู้ให้บริการมีชื่อและ URL ที่ไม่ซ้ำกัน </span><span class="sxs-lookup"><span data-stu-id="951fb-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="951fb-113">ตรวจทานเนื้อหาของหน้านี้ และข้ามกระบวนงานนี้ ถ้าเรกคอร์ดสำหรับ Litware, Inc. (https://www.litware.com) มีอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="951fb-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="951fb-114">ในฟิลด์ชื่อ ให้พิมพ์ `Litware, Inc.`</span><span class="sxs-lookup"><span data-stu-id="951fb-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="951fb-115">ในฟิลด์ที่อยู่อินเทอร์เน็ต ให้พิมพ์ `https://www.litware.com`</span><span class="sxs-lookup"><span data-stu-id="951fb-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="951fb-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="951fb-116">Select **Save**.</span></span>
8. <span data-ttu-id="951fb-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="951fb-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="951fb-118">เลือกเป็นผู้ให้บริการที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="951fb-118">Select as an active provider</span></span>
1. <span data-ttu-id="951fb-119">เลือกผู้ให้บริการ Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="951fb-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="951fb-120">เลือก **กำหนดเป็นใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="951fb-120">Select **Set active**.</span></span>

![พื้นที่ทำงานการรายงานทางอิเล็กทรอนิกส์](../media/GER-Task-ActiveProvider-1.png)
