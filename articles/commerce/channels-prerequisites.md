---
title: ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง
description: หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002300"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="8b19d-103">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8b19d-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8b19d-104">หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="8b19d-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b19d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="8b19d-105">Overview</span></span>

<span data-ttu-id="8b19d-106">ก่อนที่ช่องทาง Dynamics 365 Commerce จะสามารถสร้างได้ ต้องทำงานที่มีข้อกำหนดเบื้องต้นหลายงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="8b19d-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="8b19d-107">รายการของงานที่มีข้อกำหนดเบื้องต้นต่อไปนี้มีการจัดระเบียบตามชนิดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8b19d-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="8b19d-108">เอกสารบางอย่างยังคงถูกเขียน และลิงค์จะถูกอัพเดตเมื่อเนื้อหาใหม่ถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="8b19d-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="8b19d-109">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8b19d-109">Initialization</span></span>

- [<span data-ttu-id="8b19d-110">เตรียมใช้งานข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8b19d-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="8b19d-111">ข้อกำหนดเบื้องต้นสากลจำเป็นสำหรับชนิดช่องทางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8b19d-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="8b19d-112">กำหนดและตั้งค่าคอนฟิกโครงสร้างนิติบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b19d-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="8b19d-113">ตั้งค่าคอนฟิกลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="8b19d-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="8b19d-114">ตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="8b19d-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="8b19d-115">ตั้งค่าคอนฟิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="8b19d-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8b19d-116">ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="8b19d-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="8b19d-117">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="8b19d-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8b19d-118">ตั้งค่าลูกค้าและสมุดที่อยู่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8b19d-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="8b19d-119">ข้อกำหนดเบื้องต้นช่องทาง Retail</span><span class="sxs-lookup"><span data-stu-id="8b19d-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="8b19d-120">รหัสข้อมูลและกลุ่มรหัสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b19d-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8b19d-121">ตั้งค่าโปรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="8b19d-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="8b19d-122">ตั้งค่าสมุดที่อยู่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="8b19d-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="8b19d-123">ตั้งค่าโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="8b19d-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="8b19d-124">ตั้งค่าสถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="8b19d-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="8b19d-125">ข้อกำหนดเบื้องต้นช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8b19d-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="8b19d-126">พารามิเตอร์ศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8b19d-126">Call center parameters</span></span>
- <span data-ttu-id="8b19d-127">วิธีการขอคืนเงินของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="8b19d-127">Call center refund methods</span></span>
- <span data-ttu-id="8b19d-128">ชนิดการเช่า</span><span class="sxs-lookup"><span data-stu-id="8b19d-128">Rental types</span></span>
- <span data-ttu-id="8b19d-129">บริการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="8b19d-129">Payment services</span></span>
- <span data-ttu-id="8b19d-130">รหัสการระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="8b19d-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="8b19d-131">ข้อกำหนดเบื้องต้นช่องทางแบบออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8b19d-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="8b19d-132">สร้างโปรไฟล์ฟังก์ชันแบบออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8b19d-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="8b19d-133">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8b19d-133">Additional resources</span></span>

[<span data-ttu-id="8b19d-134">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="8b19d-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8b19d-135">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="8b19d-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="8b19d-136">การตั้งค่าลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="8b19d-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="8b19d-137">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8b19d-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="8b19d-138">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="8b19d-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="8b19d-139">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="8b19d-139">Set up an online channel</span></span>](channel-setup-online.md)
