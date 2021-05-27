---
title: บริการแบบสากล Dynamics 365
description: หัวข้อนี้แสดงภาพรวมของบริการแบบสากล Microsoft Dynamics 365
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018818"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="7dc01-103">บริการแบบสากล Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="7dc01-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7dc01-104">บริการสากลต่อไปนี้สามารถตั้งค่าคอนฟิกเพื่อขยายความสามารถที่มีอยู่ในบริการออนไลน์ Microsoft Dynamics 365 บางบริการ:</span><span class="sxs-lookup"><span data-stu-id="7dc01-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="7dc01-105">**Regulatory Configuration Service (RCS)** สนับสนุนการตั้งค่าคอนฟิกของเอกสารและรายงานอิเล็กทรอนิกส์ชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="7dc01-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="7dc01-106">RCS ให้โปรแกรมออกแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ขั้นสูง ซึ่งที่เก็บการตั้งค่าคอนฟิกคือบริการแบบสแตนด์อโลนอยู่</span><span class="sxs-lookup"><span data-stu-id="7dc01-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="7dc01-107">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Regulatory Configuration Service](rcs-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7dc01-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="7dc01-108">**การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์** จะรวมรูปแบบที่ตั้งค่าคอนฟิกได้ไว้ด้วยกันสากการแปลง ลายเซ็นดิจิทัล และการรวมที่ตั้งค่าคอนฟิกได้ เพื่อการเชื่อมต่อกับเว็บเซอร์วิสภายนอก รวมถึงการจัดการใบรับรองและการตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="7dc01-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="7dc01-109">สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](e-invoicing-service-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7dc01-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="7dc01-110">**การคํานวณภาษี** ให้ความยืดหยุ่นเพิ่มขึ้นโดยสนับสนุนหลายรหัสภาษี การกําหนดรหัสภาษี โปรแกรมออกแบบการคํานวณภาษี และกลไกจัดการรันไทม์เพื่อให้เป็นไปตามข้อบังคับด้านภาษีที่ซับซ้อนทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="7dc01-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="7dc01-111">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการคำนวณ โปรดดูที่ [การคํานวณภาษี](global-tax-calcuation-service-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7dc01-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="7dc01-112">บริการสากลเหล่านี้ให้การรวมแบบสำเร็จรูปกับบริการออนไลน์ของ Dynamics 365 ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7dc01-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="7dc01-113">บริการออนไลน์</span><span class="sxs-lookup"><span data-stu-id="7dc01-113">Online service</span></span> | <span data-ttu-id="7dc01-114">RCS</span><span class="sxs-lookup"><span data-stu-id="7dc01-114">RCS</span></span> | <span data-ttu-id="7dc01-115">การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="7dc01-115">Electronic Invoicing</span></span> | <span data-ttu-id="7dc01-116">การคำนวณภาษี (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="7dc01-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="7dc01-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7dc01-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="7dc01-118">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-118">Yes</span></span> | <span data-ttu-id="7dc01-119">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-119">Yes</span></span> | <span data-ttu-id="7dc01-120">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-120">Yes</span></span> | 
| <span data-ttu-id="7dc01-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="7dc01-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="7dc01-122">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-122">Yes</span></span> | <span data-ttu-id="7dc01-123">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-123">Yes</span></span> | <span data-ttu-id="7dc01-124">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-124">Yes</span></span> | 
| <span data-ttu-id="7dc01-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="7dc01-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="7dc01-126">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-126">Yes</span></span> | <span data-ttu-id="7dc01-127">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-127">Yes</span></span> | <span data-ttu-id="7dc01-128">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="7dc01-128">Not applicable</span></span> | 
| <span data-ttu-id="7dc01-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7dc01-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="7dc01-130">ใช่</span><span class="sxs-lookup"><span data-stu-id="7dc01-130">Yes</span></span> | <span data-ttu-id="7dc01-131">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="7dc01-131">Not applicable</span></span> | <span data-ttu-id="7dc01-132">ใช้ไม่ได้</span><span class="sxs-lookup"><span data-stu-id="7dc01-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="7dc01-133">เนื่องจากความแตกต่างในความพร้อมใช้งานของที่ตั้งทางภูมิศาสตร์ของ Azure (ภูมิศาสตร์) ของ RCS จึงทําให้การตั้งค่าคอนฟิกของบริการนี้อาจทําให้คุณสามารถโอนย้ายข้อมูลของลูกค้าภายนอกพื้นที่ที่เลือกไว้สำหรับบริการออนไลน์ของ Dynamics 365 ที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="7dc01-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="7dc01-134">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/rcs/D365Productavailabilityguide)</span><span class="sxs-lookup"><span data-stu-id="7dc01-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>