---
title: ภาพรวมของช่องทาง
description: หัวข้อนี้แสดงภาพรวมของช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800554"
---
# <a name="channels-overview"></a><span data-ttu-id="33eb8-103">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="33eb8-104">หัวข้อนี้แสดงภาพรวมของช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="33eb8-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="33eb8-105">โดยจะมีข้อมูลเกี่ยวกับภารกิจที่คุณต้องกรอกทั้งหมดก่อน และหลังจากที่คุณตั้งค่าแต่ละช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="33eb8-106">ชนิดของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-106">Types of Channels</span></span>

<span data-ttu-id="33eb8-107">Dynamics 365 Commerce รองรับช่องทางสามชนิดที่แตกต่างกัน ได้แก่ การขายปลีก ศูนย์บริการ และช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="33eb8-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="33eb8-108">ช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="33eb8-108">Retail channels</span></span>

<span data-ttu-id="33eb8-109">ช่องทางการขายปลีกแสดงถึงร้านค้าจริงมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="33eb8-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="33eb8-110">ร้านค้าแต่ละร้านสามารถมีทะเบียนการขายหน้าร้าน (POS) ของตนเอง เงินได้ และบัญชีค่าใช้จ่าย และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="33eb8-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="33eb8-111">ช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="33eb8-111">Call center channels</span></span>

<span data-ttu-id="33eb8-112">ช่องทางของศูนย์บริการแสดงถึงใบสั่งศูนย์บริการ และการจัดการลูกค้า</span><span class="sxs-lookup"><span data-stu-id="33eb8-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="33eb8-113">ช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="33eb8-113">Online channels</span></span>

<span data-ttu-id="33eb8-114">ช่องทางออนไลน์แสดงถึงหน้าร้านพาณิชย์อิเล็กทรอนิกส์แบบออนไลน์</span><span class="sxs-lookup"><span data-stu-id="33eb8-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="33eb8-115">เมื่อมีการสร้างช่องทางออนไลน์ จะต้องสร้างไซต์โดยใช้โปรแกรมสร้างไซต์ Microsoft Microsoft Dynamics 365 Commerce หรือโซลูชันพาณิชย์อิเล็กทรอนิกส์อื่น ๆ ของบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="33eb8-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="33eb8-116">ข้อมูลพื้นฐานเกี่ยวกับการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-116">Channel setup basics</span></span>

<span data-ttu-id="33eb8-117">การตั้งค่าช่องทางดำเนินการในเครื่องมือ Commerce</span><span class="sxs-lookup"><span data-stu-id="33eb8-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="33eb8-118">แต่ละช่องทางสามารถมีวิธีการชำระเงินของตนเอง กลุ่มราคา ลำดับชั้นของผลิตภัณฑ์ การจัดประเภท และชุดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="33eb8-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="33eb8-119">หลังจากที่คุณสร้างช่องทางแล้ว กำหนดผลิตภัณฑ์ที่คุณต้องการดำเนินการและขาย</span><span class="sxs-lookup"><span data-stu-id="33eb8-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="33eb8-120">แต่ละชนิดของช่องทางมีชุดของลักษณะการทำงานเฉพาะที่อาจจำเป็นต้องได้รับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="33eb8-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="33eb8-121">ตัวอย่างเช่น ช่องทางการขายปลีกจำเป็นต้องมีการกำหนดพนักงาน ทะเบียน และลูกค้า</span><span class="sxs-lookup"><span data-stu-id="33eb8-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="33eb8-122">เมื่อสร้างช่องทางใหม่แล้ว ต้องกำหนดให้กับลำดับชั้นขององค์กรด้วย</span><span class="sxs-lookup"><span data-stu-id="33eb8-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="33eb8-123">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-123">Channel setup prerequisites</span></span>

<span data-ttu-id="33eb8-124">ก่อนที่คุณจะสามารถตั้งค่าช่องทางได้ คุณต้องทำข้อกำหนดเบื้องต้นบางอย่างตามชนิดช่องทางให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="33eb8-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="33eb8-125">สำหรับข้อมูลเพิ่มเติม ดูที่ [ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง](channels-prerequisites.md)</span><span class="sxs-lookup"><span data-stu-id="33eb8-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="33eb8-126">ตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-126">Set up a channel</span></span>

<span data-ttu-id="33eb8-127">หลังจากที่คุณทำงานที่เป็นข้อกำหนดเบื้องต้นเสร็จสมบูรณ์แล้ว สำหรับคำแนะนำการตั้งค่าเพิ่มเติม ให้ใช้ลิงค์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="33eb8-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="33eb8-128">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="33eb8-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="33eb8-129">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="33eb8-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="33eb8-130">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="33eb8-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="33eb8-131">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="33eb8-131">Additional resources</span></span>

[<span data-ttu-id="33eb8-132">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="33eb8-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="33eb8-133">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="33eb8-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="33eb8-134">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="33eb8-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="33eb8-135">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="33eb8-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="33eb8-136">การตั้งค่าลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="33eb8-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]