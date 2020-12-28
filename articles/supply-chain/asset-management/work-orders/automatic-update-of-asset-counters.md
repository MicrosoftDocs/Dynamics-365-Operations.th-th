---
title: การอัปเดตตัวนับสินทรัพย์อัตโนมัติ
description: หัวข้อนี้อธิบายการอัปเดตตัวนับสินทรัพย์อัตโนมัติในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438305"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="f2b94-103">การอัปเดตตัวนับสินทรัพย์อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f2b94-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2b94-104">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการลงทะเบียนตัวนับทางสินทรัพย์ ดูที่ [การอัพเดตตัวนับทางสินทรัพย์ด้วยตนเอง](../work-orders/manual-update-of-asset-counters.md)</span><span class="sxs-lookup"><span data-stu-id="f2b94-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="f2b94-105">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าตัวนับทางสินทรัพย์ ดูที่ [ตัวนับ](../setup-for-objects/counters.md)</span><span class="sxs-lookup"><span data-stu-id="f2b94-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="f2b94-106">ค่าตัวนับยังสามารถได้รับการอัพเดตจากการลงทะเบียนการผลิตโดยอัตโนมัติ ตามชั่วโมงการผลิตหรือปริมาณการผลิต (กล่าวคือ มีการผลิตปริมาณแล้ว)</span><span class="sxs-lookup"><span data-stu-id="f2b94-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="f2b94-107">การอัพเดตนี้จะดำเนินการบนเพจ **อัพเดตตัวนับทางสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f2b94-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="f2b94-108">คุณสามารถอัพเดตหนึ่งสินทรัพย์หรือหลายสินทรัพย์ได้โดยการตั้งค่าหนึ่งพารามิเตอร์ **วันที่เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="f2b94-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="f2b94-109">พารามิเตอร์นี้จะระบุวันที่เริ่มต้นสำหรับการลงทะเบียนการผลิต (ชั่วโมงการผลิตหรือปริมาณการผลิต)</span><span class="sxs-lookup"><span data-stu-id="f2b94-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="f2b94-110">กล่าวคือ พารามิเตอร์จะระบุวันที่ที่จะค่าของตัวนับจะใช้อัพเดต</span><span class="sxs-lookup"><span data-stu-id="f2b94-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="f2b94-111">สินทรัพย์ทั้งหมดที่เกี่ยวข้องกับทรัพยากร *และ* มีตัวนับสินทรัพย์ที่มีการตั้งค่าให้อัพเดตโดยยึดตามชั่วโมงการผลิตหรือปติมาณที่ผลิต จะถูกรวมไว้ในการอัพเดตอัตโนมัติ และจะมีการสร้างค่าตัวนับใหม่</span><span class="sxs-lookup"><span data-stu-id="f2b94-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="f2b94-112">ค่าตัวนับใหม่จะมีการสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f2b94-112">New counter values will be created.</span></span>

<span data-ttu-id="f2b94-113">สำหรับตัวนับที่ยึดตามปริมาณการผลิต จะมีการตรวจนับทั้งปริมาณสินค้าที่ดีและปริมาณสินค้าที่บกพร่องที่มีการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="f2b94-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="f2b94-114">หากหน่วยที่ใช้สำหรับการลงทะเบียนปริมาณการผลิต แตกต่างจากหน่วยที่ใช้ในตัวนับ ปริมาณจะมีการแปลงเพื่อให้สอดคล้อบกับหน่วยตัวนับ</span><span class="sxs-lookup"><span data-stu-id="f2b94-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="f2b94-115">ดังกล่าวข้างต้น ตัวนับอัตโนมัติสามารถได้รับการอัพเดตจากการลงทะเบียนการผลิตได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="f2b94-116">ดังนั้น สินทรัพย์ที่คุณต้องการให้อัพเดตตัวนับโดยอัตโนมัติต้องสัมพันธ์กับทรัพยากร (เครื่องจักร)</span><span class="sxs-lookup"><span data-stu-id="f2b94-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="f2b94-117">เมื่อปริมาณที่ผลิตหรือชั่วโมงการผลิตได้รับการลงทะเบียนในทรัพยากรแล้ว คุณสามารถอัพเดตตัวนับสินทรัพย์ที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="f2b94-118">เลือก **การจัดการสินทรัพย์** > **ประจำงวด** > **สินทรัพย์** > **อัพเดตตัวนับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f2b94-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="f2b94-119">ในฟิลด์ **วันที่เริ่มต้น** เลือกวันที่เริ่มต้นของการอัพเดตอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f2b94-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="f2b94-120">วันที่ในฟิลด์นี้เป็นวันที่ "งานระหว่างทำ" จาก **ธุรกรรมกระบวนการผลิต** (**การควบคุมการผลิต** > **การสอบถามและรายงาน** > **การผลิต** > **ธุรกรรมกระบวนการผลิต** > ฟิลด์ **วันที่ทางกายภาพ** )</span><span class="sxs-lookup"><span data-stu-id="f2b94-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="f2b94-121">บนแท็บด่วน **เรกคอร์ดที่จะรวม** คุณสามารถเลือกสินทรัพย์ ชนิดสินทรัพย์ หรือทรัพยากรสำหรับการอัพเดตอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f2b94-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="f2b94-122">เลือก **ตัวกรอง** และทำการเลือกที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f2b94-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="f2b94-123">บน FastTab **รันในเบื้องหลัง** คุณสามารถตั้งค่าการปรับปรุงอัตโนมัติเป็นชุดงานได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f2b94-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="f2b94-124">ภาพประกอบด้านล่างแสดงตัวอย่างของกล่องโต้ตอบ **อัพเดตตัวนับทางสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f2b94-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![รูปที่ 1](media/12-work-orders.png)

5. <span data-ttu-id="f2b94-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f2b94-126">Select **OK**.</span></span> 

<span data-ttu-id="f2b94-127">หลังจากอัพเดตตัวนับทางสินทรัพย์อัตโนมัติแล้ว คุณสามารถดูการลงทะเบียนตัวนับที่เกี่ยวข้องกับสินทรัพย์บนเพจ **ตัวนับทางสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f2b94-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="f2b94-128">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **สินทรัพย์** > **สินทรัพย์ทั้งหมด** เลือกสินทรัพย์ จากนั้นบนบานหน้าต่างการดำเนินการบนแท็บ **สินทรัพย์** ในกลุ่ม **เชิงป้องกัน** เลือก **Counters**</span><span class="sxs-lookup"><span data-stu-id="f2b94-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="f2b94-129">บนเพจ **มูลค่ารวมของสินทรัพย์ได้** คุณสามารถดูภาพรวมของการลงทะเบียนล่าสุดที่มีการทำบนชนิดตัวนับทั้งหมดในสินทรัพย์ทั้งหมดได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="f2b94-130">เลือก **การจัดการสินทรัพย์** > **การสอบถาม** > **สินทรัพย์** > **มูลค่ารวมของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="f2b94-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="f2b94-131">เพจนี้จะคล้ายกับเพจ **ตัวนับทางสินทรัพย์** แต่คุณไม่สามารถเพิ่มหรือแก้ไขการลงทะเบียนได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="f2b94-132">มีไว้เพื่อดูภาพรวมเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f2b94-132">It's for overview only.</span></span>

<span data-ttu-id="f2b94-133">ภาพประกอบด้านล่างแสดงตัวอย่างของหน้า **มูลค่ารวมของสินทรัพย์ได้**</span><span class="sxs-lookup"><span data-stu-id="f2b94-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![รูปที่ 2](media/13-work-orders.png)

<span data-ttu-id="f2b94-135">บันทึกคะแนนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f2b94-135">Note the following points:</span></span>

- <span data-ttu-id="f2b94-136">คุณสามารถสร้างการลงทะเบียนค่าตัวนับด้วยตนเองสำหรับชนิดตัวนับที่มีการอัพเดตโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="f2b94-137">สำหรับข้อมูลเพิ่มเติม ดูที่ [การอัพเดตตัวนับทางสินทรัพย์ด้วยตนเอง](../work-orders/manual-update-of-asset-counters.md)</span><span class="sxs-lookup"><span data-stu-id="f2b94-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="f2b94-138">คุณสามารถตั้งค่าตัวนับที่เกี่ยวข้องกับตัวนับอื่นได้</span><span class="sxs-lookup"><span data-stu-id="f2b94-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="f2b94-139">ในกรณีนี้ เมื่อมีการอัพเดตตัวนับ ตัวนับที่เกี่ยวข้องจะมีการอัพเดตโดยอัตโนมัติในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f2b94-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="f2b94-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าตัวนับที่เกี่ยวข้อง ดูที่ [ตัวนับ](../setup-for-objects/counters.md)</span><span class="sxs-lookup"><span data-stu-id="f2b94-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

