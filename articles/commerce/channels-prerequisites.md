---
title: ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง
description: หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997711"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="edcc0-103">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="edcc0-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="edcc0-104">หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="edcc0-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="edcc0-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="edcc0-105">Overview</span></span>

<span data-ttu-id="edcc0-106">ก่อนที่ช่องทาง Dynamics 365 Commerce จะสามารถสร้างได้ ต้องทำงานที่มีข้อกำหนดเบื้องต้นหลายงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="edcc0-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="edcc0-107">รายการของงานที่มีข้อกำหนดเบื้องต้นต่อไปนี้มีการจัดระเบียบตามชนิดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="edcc0-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="edcc0-108">เอกสารบางอย่างยังคงถูกเขียน และลิงค์จะถูกอัพเดตเมื่อเนื้อหาใหม่ถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="edcc0-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="edcc0-109">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="edcc0-109">Initialization</span></span>

- [<span data-ttu-id="edcc0-110">เตรียมใช้งานข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="edcc0-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="edcc0-111">ข้อกำหนดเบื้องต้นสากลจำเป็นสำหรับชนิดช่องทางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="edcc0-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="edcc0-112">กำหนดและตั้งค่าคอนฟิกโครงสร้างนิติบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="edcc0-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="edcc0-113">ตั้งค่าคอนฟิกลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="edcc0-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="edcc0-114">ตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="edcc0-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="edcc0-115">ตั้งค่าคอนฟิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="edcc0-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="edcc0-116">ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="edcc0-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="edcc0-117">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="edcc0-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="edcc0-118">ตั้งค่าลูกค้าและสมุดที่อยู่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="edcc0-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="edcc0-119">ข้อกำหนดเบื้องต้นช่องทาง Retail</span><span class="sxs-lookup"><span data-stu-id="edcc0-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="edcc0-120">รหัสข้อมูลและกลุ่มรหัสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="edcc0-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="edcc0-121">ตั้งค่าโปรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="edcc0-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="edcc0-122">ตั้งค่าสมุดที่อยู่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="edcc0-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="edcc0-123">ตั้งค่าโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="edcc0-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="edcc0-124">ตั้งค่าสถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="edcc0-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="edcc0-125">ข้อกำหนดเบื้องต้นช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="edcc0-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="edcc0-126">พารามิเตอร์ศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="edcc0-126">Call center parameters</span></span>
- [<span data-ttu-id="edcc0-127">วิธีการชำระเงินตามใบสั่งของศูนย์บริการและการเรียกคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="edcc0-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="edcc0-128">โหมดศูนย์บริการของการจัดส่งและค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="edcc0-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="edcc0-129">ข้อกำหนดเบื้องต้นของช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="edcc0-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="edcc0-130">สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="edcc0-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="edcc0-131">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="edcc0-131">Additional resources</span></span>

[<span data-ttu-id="edcc0-132">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="edcc0-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="edcc0-133">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="edcc0-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="edcc0-134">การตั้งค่าลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="edcc0-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="edcc0-135">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="edcc0-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="edcc0-136">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="edcc0-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="edcc0-137">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="edcc0-137">Set up an online channel</span></span>](channel-setup-online.md)
