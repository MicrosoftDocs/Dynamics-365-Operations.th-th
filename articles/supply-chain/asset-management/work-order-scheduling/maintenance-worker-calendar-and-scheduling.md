---
title: ปฏิทินและการจัดกำหนดการเจ้าหน้าที่บำรุงรักษา
description: หัวข้อนี้จะอธิบายถึงปฏิทินของเจ้าหน้าที่บำรุงรักษาโดยสัมพันธ์กับการจัดกำหนดการในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c8856d0c7a7b76318755dc6bcdbb1859de1fa20a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021490"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="4ba44-103">ปฏิทินและการจัดกำหนดการเจ้าหน้าที่บำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4ba44-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4ba44-104">เมื่อคุณจัดกำหนดการใบสั่งงาน คุณสร้างกำหนดการสำหรับเจ้าหน้าที่บำรุงรักษา เครื่องมือ และสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4ba44-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="4ba44-105">เพื่อที่จะจัดกำหนดการเจ้าหน้าที่บำรุงรักษา จะต้องมีการตั้งค่าปฏิทินสำหรับเจ้าหน้าที่บำรุงรักษาแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="4ba44-105">In order to schedule maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="4ba44-106">เจ้าหน้าที่บำรุงรักษาเกี่ยวข้องกับทรัพยากร และปฏิทินเวลาการทำงานถูกตั้งค่าสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4ba44-106">Maintenance workers are related to a resource, and working time calendars are set up for resources.</span></span> <span data-ttu-id="4ba44-107">คุณตั้งค่าทรัพยากรและปฏิทินใน **การจัดการสินทรัพย์** > **การตั้งค่า** > **ผู้ปฏิบัติงาน** > **ผู้ปฏิบัติงาน** ซึ่งอธิบายไว้ใน [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)</span><span class="sxs-lookup"><span data-stu-id="4ba44-107">You set up the resource and calendar in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="4ba44-108">ภาพหน้าจอด้านล่างแสดงตัวอย่างของเจ้าหน้าที่บำรุงรักษาที่เกี่ยวข้องกับทรัพยากรที่ใช้ปฏิทินเวลาการทำงาน "การผลิต"</span><span class="sxs-lookup"><span data-stu-id="4ba44-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![รูปที่ 1](media/01-work-order-scheduling.png)

<span data-ttu-id="4ba44-110">ไม่จำเป็นต้องมีการตั้งค่าปฏิทินสำหรับเครื่องมือและสินทรัพย์โดยสัมพันธ์กับการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="4ba44-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="4ba44-111">สมมติฐานคือ เครื่องมือและสินทรัพย์พร้อมใช้งาน 24 ชั่วโมงต่อวันสำหรับการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="4ba44-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>

