---
title: เก็บถาวรใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาด้วยหมายเลขแฮช
description: หัวข้อนี้อธิบายวิธีการเปิดใช้งานการเก็บถาวรเพื่อจัดเก็บใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาพร้อมหมายเลขแฮช
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557491"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="40b44-103">เก็บถาวรใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาด้วยหมายเลขแฮช</span><span class="sxs-lookup"><span data-stu-id="40b44-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="40b44-104">ในบางประเทศ มีข้อกําหนดทางกฎหมายในการจัดเก็บหมายเลขแฮชที่คํานวณได้ในระบบร่วมกับการพิมพ์เอกสารบางฉบับ</span><span class="sxs-lookup"><span data-stu-id="40b44-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="40b44-105">สามารถใช้หมายเลขแฮชเพื่อรายงานต่อหน่วยงานจัดเก็บภาษีและในระหว่างการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="40b44-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="40b44-106">หัวข้อนี้อธิบายวิธีการกำหนดค่าการเก็บถาวรเพื่อจัดเก็บใบแจ้งหนี้ของลูกค้าที่พิมพ์ออกมาพร้อมหมายเลขแฮช</span><span class="sxs-lookup"><span data-stu-id="40b44-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="40b44-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="40b44-107">Prerequisites</span></span>

- <span data-ttu-id="40b44-108">ในพื้นที่ **จัดการลักษณะ** ให้เปิดคุณสมบัติ **ใบกำกับสินค้าที่พิมพ์พร้อมด้วยหมายเลขแฮช**</span><span class="sxs-lookup"><span data-stu-id="40b44-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="40b44-109">สำหรับข้อมูลเพิ่มเติม ดูที่ [ภาพรวมการจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="40b44-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="40b44-110">ต้องตั้งค่าคอนฟิกรูปแบบที่สามารถพิมพ์ได้ของเอกสารที่กําหนดใน **การจัดการการพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="40b44-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="40b44-111">ฟังก์ชันนี้สามารถใช้ได้กับเอกสารต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="40b44-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="40b44-112">**บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="40b44-112">**Accounts receivable**</span></span>
- <span data-ttu-id="40b44-113">ใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40b44-113">Customer invoice</span></span>
- <span data-ttu-id="40b44-114">ใบลดหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40b44-114">Customer credit note</span></span>
- <span data-ttu-id="40b44-115">ใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="40b44-115">Free text invoice</span></span>
- <span data-ttu-id="40b44-116">ใบลดหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="40b44-116">Free text credit note</span></span>

<span data-ttu-id="40b44-117">**การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="40b44-117">**Project management and accounting**</span></span>
- <span data-ttu-id="40b44-118">ใบแจ้งหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="40b44-118">Project invoice</span></span>
- <span data-ttu-id="40b44-119">ใบลดหนี้ของโครงการ</span><span class="sxs-lookup"><span data-stu-id="40b44-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="40b44-120">กำหนดค่าข้อมูลหลักของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="40b44-120">Configure customer master data</span></span>
<span data-ttu-id="40b44-121">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกข้อมูลลูกค้าและเปิดความสามารถในการบันทึกใบแจ้งหนี้ที่พิมพ์เป็นเอกสารแนบโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="40b44-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="40b44-122">ไปที่ **บัญชีลูกหนี้** > **ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="40b44-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="40b44-123">เลือกลูกค้า และบน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในส่วน **E-INVOCE** ในฟิลด์ **เอกสารแนบ eInvoice** ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="40b44-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="40b44-124">พิมพ์ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="40b44-124">Print invoices</span></span>
<span data-ttu-id="40b44-125">คุณสามารถลงรายการบัญชีและพิมพ์ข้อความอิสระ ลูกค้า และใบแจ้งหนี้โครงการ หรือใบลดหนี้ใดๆ ของลูกค้าที่กำหนดค่าคอนฟิกในกระบวนการก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="40b44-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="40b44-126">เปิดหน้า **เอกสารแนบ** ของใบแจ้งหนี้ที่พิมพ์ออกมา</span><span class="sxs-lookup"><span data-stu-id="40b44-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="40b44-127">บน FastTab **เอกสารแนบ** ในกลุ่มฟิลด์ **รายละเอียดเพิ่มเติม** ในฟิลด์ **หมายเลขเอกสารแฮช** ให้ค้นหาหมายเลขแฮชที่จัดเก็บซึ่งคํานวณไว้สำหรับใบแจ้งหนี้ที่พิมพ์ออกมา</span><span class="sxs-lookup"><span data-stu-id="40b44-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![หมายเลขแฮชของเอกสารแนบ](media/attach-hash-num.jpg)

