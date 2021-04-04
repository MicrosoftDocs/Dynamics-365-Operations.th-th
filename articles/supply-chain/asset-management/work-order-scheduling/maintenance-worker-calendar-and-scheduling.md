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
ms.openlocfilehash: ada3ab1afb5b9989510324148a6f26b215a200d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252905"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a><span data-ttu-id="e209f-103">ปฏิทินและการจัดกำหนดการเจ้าหน้าที่บำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e209f-103">Maintenance worker calendar and scheduling</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e209f-104">เมื่อคุณจัดกำหนดการใบสั่งงาน คุณสร้างกำหนดการสำหรับเจ้าหน้าที่บำรุงรักษา เครื่องมือ และสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e209f-104">When you schedule work orders, you create a schedule for maintenance workers, tools, and assets.</span></span> <span data-ttu-id="e209f-105">เพื่อที่จะจัดกำหนดการเจ้าหน้าที่บำรุงรักษา จะต้องมีการตั้งค่าปฏิทินสำหรับเจ้าหน้าที่บำรุงรักษาแต่ละคน</span><span class="sxs-lookup"><span data-stu-id="e209f-105">In order to schedule maintenance workers, a calendar must be set up for each maintenance worker.</span></span> <span data-ttu-id="e209f-106">เจ้าหน้าที่บำรุงรักษาเกี่ยวข้องกับทรัพยากร และปฏิทินเวลาการทำงานถูกตั้งค่าสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="e209f-106">Maintenance workers are related to a resource, and working time calendars are set up for resources.</span></span> <span data-ttu-id="e209f-107">คุณตั้งค่าทรัพยากรและปฏิทินใน **การจัดการสินทรัพย์** > **การตั้งค่า** > **ผู้ปฏิบัติงาน** > **ผู้ปฏิบัติงาน** ซึ่งอธิบายไว้ใน [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)</span><span class="sxs-lookup"><span data-stu-id="e209f-107">You set up the resource and calendar in **Asset management** > **Setup** > **Workers** > **Workers**, which is described in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

<span data-ttu-id="e209f-108">ภาพหน้าจอด้านล่างแสดงตัวอย่างของเจ้าหน้าที่บำรุงรักษาที่เกี่ยวข้องกับทรัพยากรที่ใช้ปฏิทินเวลาการทำงาน "การผลิต"</span><span class="sxs-lookup"><span data-stu-id="e209f-108">The screenshot below shows an example of a maintenance worker who is related to a resource that uses the working time calendar "Production".</span></span>

![รูปที่ 1](media/01-work-order-scheduling.png)

<span data-ttu-id="e209f-110">ไม่จำเป็นต้องมีการตั้งค่าปฏิทินสำหรับเครื่องมือและสินทรัพย์โดยสัมพันธ์กับการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e209f-110">Calendar setup for tools and assets is not needed in relation to work order scheduling.</span></span> <span data-ttu-id="e209f-111">สมมติฐานคือ เครื่องมือและสินทรัพย์พร้อมใช้งาน 24 ชั่วโมงต่อวันสำหรับการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e209f-111">The assumption is that tools and assets are available 24 hours a day for maintenance.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]