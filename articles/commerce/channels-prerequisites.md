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
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477935"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="9db5a-103">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9db5a-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9db5a-104">หัวข้อนี้แสดงภาพรวมของข้อกำหนดเบื้องต้นในการตั้งค่าช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9db5a-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9db5a-105">ก่อนที่ช่องทาง Dynamics 365 Commerce จะสามารถสร้างได้ ต้องทำงานที่มีข้อกำหนดเบื้องต้นหลายงานให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="9db5a-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="9db5a-106">รายการของงานที่มีข้อกำหนดเบื้องต้นต่อไปนี้มีการจัดระเบียบตามชนิดช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9db5a-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="9db5a-107">เอกสารบางอย่างยังคงถูกเขียน และลิงค์จะถูกอัพเดตเมื่อเนื้อหาใหม่ถูกเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="9db5a-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="9db5a-108">การเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9db5a-108">Initialization</span></span>

- [<span data-ttu-id="9db5a-109">เตรียมใช้งานข้อมูลเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="9db5a-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="9db5a-110">ข้อกำหนดเบื้องต้นสากลจำเป็นสำหรับชนิดช่องทางทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9db5a-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="9db5a-111">กำหนดและตั้งค่าคอนฟิกโครงสร้างนิติบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="9db5a-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="9db5a-112">ตั้งค่าคอนฟิกลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="9db5a-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="9db5a-113">ตั้งค่าคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9db5a-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="9db5a-114">ตั้งค่าคอนฟิกภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="9db5a-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="9db5a-115">ตั้งค่าโปรไฟล์การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="9db5a-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="9db5a-116">ตั้งค่าลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="9db5a-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="9db5a-117">ตั้งค่าลูกค้าและสมุดที่อยู่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9db5a-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="9db5a-118">ข้อกำหนดเบื้องต้นช่องทาง Retail</span><span class="sxs-lookup"><span data-stu-id="9db5a-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="9db5a-119">รหัสข้อมูลและกลุ่มรหัสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="9db5a-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="9db5a-120">ตั้งค่าโปรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="9db5a-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="9db5a-121">ตั้งค่าสมุดที่อยู่พนักงาน</span><span class="sxs-lookup"><span data-stu-id="9db5a-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="9db5a-122">ตั้งค่าโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="9db5a-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="9db5a-123">ตั้งค่าสถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="9db5a-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="9db5a-124">ข้อกำหนดเบื้องต้นช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="9db5a-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="9db5a-125">พารามิเตอร์ศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="9db5a-125">Call center parameters</span></span>
- [<span data-ttu-id="9db5a-126">วิธีการชำระเงินตามใบสั่งของศูนย์บริการและการเรียกคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="9db5a-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="9db5a-127">โหมดศูนย์บริการของการจัดส่งและค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="9db5a-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="9db5a-128">ข้อกำหนดเบื้องต้นของช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="9db5a-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="9db5a-129">สร้างโพรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="9db5a-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="9db5a-130">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9db5a-130">Additional resources</span></span>

[<span data-ttu-id="9db5a-131">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9db5a-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9db5a-132">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="9db5a-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9db5a-133">การตั้งค่าลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="9db5a-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="9db5a-134">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="9db5a-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="9db5a-135">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="9db5a-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="9db5a-136">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="9db5a-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
