---
title: เลือกชุดงานที่เก่าที่สุดบนอุปกรณ์เคลื่อนที่
description: หัวข้อนี้อธิบายวิธีตั้งค่าและใช้ตัวเลือกการเลือกชุดงานที่เก่าที่สุดจากอุปกรณ์เคลื่อนที่
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438363"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="1fadc-103">เลือกชุดงานที่เก่าที่สุดบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1fadc-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fadc-104">คุณสามารถเข้าถึงการตั้งค่าคอนฟิก **เลือกชุดงานที่เก่าที่สุด** ผ่านทางเมนูอุปกรณ์เคลื่อนที่ และช่วยให้คุณสามารถบังคับหรือเตือนผู้ปฏิบัติงานคลังสินค้าให้เลือกชุดงานที่เก่าที่สุดในตำแหน่งปัจจุบันของตนได้</span><span class="sxs-lookup"><span data-stu-id="1fadc-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="1fadc-105">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="1fadc-105">Where it applies</span></span>
<span data-ttu-id="1fadc-106">เลือกชุดงานที่เก่าที่สุดได้รับการตั้งค่าคอนฟิกบนรายการเมนูของอุปกรณ์เคลื่อนที่ และส่งผลต่อการเลือกชุดงานด้านล่างรายการ</span><span class="sxs-lookup"><span data-stu-id="1fadc-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="1fadc-107">วิธีการตั้งค่าการตั้งค่าคอนฟิกสำหรับ เลือกชุดงานที่เก่าที่สุด</span><span class="sxs-lookup"><span data-stu-id="1fadc-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="1fadc-108">สำหรับสินค้าที่กำหนดให้ใช้งานที่มีอยู่ **เลือกชุดงานที่เก่าที่สุด** สามารถตั้งค่าเป็น **ไม่มี** **เตือน** หรือ **บังคับ** จากเมนูอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="1fadc-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="1fadc-109">**ไม่มี**: ผู้ปฏิบัติงานจะไม่ได้รับข้อความใด ๆ และจะสามารถเลือกชุดงานใด ๆ ในตำแหน่งของตน</span><span class="sxs-lookup"><span data-stu-id="1fadc-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="1fadc-110">**เตือน** และ **บังคับ**: รายการของชุดงานที่มีวันหมดอายุที่เก่าที่สุดจะแสดงอยู่เหนือการควบคุมชุดงานเมื่อผู้ปฏิบัติงานเลือกชุดงาน</span><span class="sxs-lookup"><span data-stu-id="1fadc-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="1fadc-111">ถ้าสถานที่มีการควบคุมป้ายทะเบียน รายการของป้ายทะเบียนที่มีชุดงานที่เก่าที่สุดจะแสดงอยู่เหนือการควบคุมป้ายทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1fadc-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="1fadc-112">**เตือน**: ถ้าผู้ปฏิบัติงานเลือกป้ายทะเบียนหรือชุดงานที่ไม่ได้อยู่ในรายการที่แสดง การควบคุมจะว่างเปล่า และจะมีการแสดงคำเตือนว่าไม่มีชุดงานที่เก่ากว่าที่จะเลือกได้</span><span class="sxs-lookup"><span data-stu-id="1fadc-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="1fadc-113">เมื่อต้องการให้สามารถดำเนินการงานต่อไป ผู้ปฏิบัติงานสามารถเลือกป้ายทะเบียนหรือชุดงานเดิมอีกครั้งได้</span><span class="sxs-lookup"><span data-stu-id="1fadc-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="1fadc-114">**หน่วยงาน**: ผู้ปฏิบัติงานจะได้รับข้อความว่ามีชุดงานที่เก่ากว่าที่จะเลือกต่อไป</span><span class="sxs-lookup"><span data-stu-id="1fadc-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>
