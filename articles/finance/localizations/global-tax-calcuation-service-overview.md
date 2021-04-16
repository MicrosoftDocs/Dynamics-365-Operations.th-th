---
title: บริการคำนวณภาษี (พรีวิว)
description: หัวข้อนี้อธิบายขอบเขตและคุณลักษณะโดยรวมของบริการคํานวณภาษี
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818235"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="6e4e9-103">บริการคำนวณภาษี (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6e4e9-104">บริการคํานวณภาษีคือบริการเช่าแบบไฮเปอร์ซึ่งทำให้ Global Tax Engine เป็นแบบอัตโนมัติ และทำให้กระบวนการในการกำหนดและการคำนวณภาษีง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="6e4e9-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="6e4e9-105">กลไกจัดการภาษีสามารถตั้งค่าคอนฟิกได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6e4e9-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="6e4e9-106">องค์ประกอบที่สามารถตั้งค่าคอนฟิกได้รวมถึง แต่ไม่จํากัดต่อ รูปแบบข้อมูลที่ต้องเสียภาษี รหัสภาษี เมทริกซ์การใช้งานภาษี และสูตรการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="6e4e9-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="6e4e9-107">กลไกจัดการภาษีจะรันบนแพลตฟอร์มบริการหลัก Microsoft Azure และนำเสนอเทคโนโลยีสมัยใหม่และความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="6e4e9-108">บริการคํานวณภาษีรวมกับ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e4e9-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6e4e9-109">ในที่สุด จะยังรวมกับ Dynamics 365 Project Operations และ Dynamics 365 Commerce และแอปพลิเคชันอื่นๆ ของบุคคลที่หนึ่งและบุคคลที่สามด้วย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="6e4e9-110">บริการคํานวณภาษีคือกลไกจัดการภาษีที่ใช้ Microsoft ที่นำเสนอความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="6e4e9-111">ซึ่งสามารถช่วยคุณในการดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e4e9-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="6e4e9-112">ตั้งค่าคอนฟิกบริการคํานวณภาษีผ่าน Regulatory Configuration Service (RCS)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="6e4e9-113">RCS เป็นรุ่นขั้นสูงของโปรแกรมออกแบบการรายงานทางอิเล็กทรอนิกส์ (ER) และพร้อมใช้งานในฐานะบริการแบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="6e4e9-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="6e4e9-114">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดรหัสและอัตราภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="6e4e9-115">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดหมายเลขทะเบียนภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="6e4e9-116">ตั้งค่าคอนฟิกโปรแกรมออกแบบการคํานวณภาษี เพื่อกําหนดสูตรและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="6e4e9-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="6e4e9-117">ใช้โซลูชันการกําหนดและการคํานวณภาษีระหว่างนิติบุคคลร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="6e4e9-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="6e4e9-118">หากต้องการใช้บริการคํานวณภาษี ให้ติดตั้ง Add-in ของบริการคํานวณภาษีจากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6e4e9-119">จากนั้น ให้ดำเนินการตั้งค่าใน RCS เสร็จสิ้น และเปิดใช้งานบริการคํานวณภาษีใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6e4e9-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="6e4e9-120">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เริ่มต้นใช้งานบริการภาษี](https://go.microsoft.com/fwlink/?linkid=2138482)</span><span class="sxs-lookup"><span data-stu-id="6e4e9-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="6e4e9-121">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6e4e9-121">Availability</span></span>

<span data-ttu-id="6e4e9-122">บริการคํานวณภาษีพร้อมใช้งานเฉพาะในสภาพแวดล้อม Sandbox และกับลูกค้าที่เลือกเท่านั้น โดยผ่านโปรแกรมพรีวิวสำหรับสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="6e4e9-123">ในที่สุด จะพร้อมใช้งานโดยทั่วไปให้แก่ลูกค้าและในสภาพแวดล้อมการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6e4e9-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="6e4e9-124">คุณลักษณะใหม่จะยังคงมีการจัดส่งในบริการคํานวณภาษีต่อไป</span><span class="sxs-lookup"><span data-stu-id="6e4e9-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="6e4e9-125">ดังนั้น รวจสอบให้แน่ใจว่าคู่มือล่าสุดมักจะทราบเกี่ยวกับความครอบคลุมและขอบเขตของคุณลักษณะที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6e4e9-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="6e4e9-126">บริการคํานวณภาษีถูกปรับใช้ในภูมิศาสตร์ Azure ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6e4e9-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="6e4e9-127">นอกจากนี้ ยังจะถูกปรับใช้กับภูมิศาสตร์ Azure เพิ่มเติม ตามความต้องการของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="6e4e9-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="6e4e9-128">สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-128">United States</span></span>
- <span data-ttu-id="6e4e9-129">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="6e4e9-129">Europe</span></span>
- <span data-ttu-id="6e4e9-130">ฝรั่งเศส</span><span class="sxs-lookup"><span data-stu-id="6e4e9-130">France</span></span>
- <span data-ttu-id="6e4e9-131">สหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="6e4e9-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="6e4e9-132">บริการคํานวณภาษีไม่สนับสนุนการปรับใช้ในสถานที่ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="6e4e9-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="6e4e9-133">นอกจากนี้ ยังไม่สนับสนุนรุ่นก่อนหน้านี้ด้วย เช่น Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="6e4e9-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="6e4e9-134">จุดเด่นของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-134">Feature highlights</span></span>

- <span data-ttu-id="6e4e9-135">เมทริกซ์ภาษีที่ตั้งค่าคอนฟิกได้เพื่อกําหนดและคํานวณภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="6e4e9-136">การสนับสนุนสำหรับหมายเลขทะเบียนภาษีมูลค่าเพิ่ม (VAT) หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e4e9-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="6e4e9-137">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดและการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="6e4e9-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="6e4e9-138">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดหมายเลขทะเบียน VAT หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e4e9-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="6e4e9-139">ธุรกรรมที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="6e4e9-139">Supported transactions</span></span>

<span data-ttu-id="6e4e9-140">สามารถเปิดใช้งานบริการคํานวณภาษีได้โดยนิติบุคคลและธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6e4e9-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="6e4e9-141">มีการสนับสนุนธุรกรรมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6e4e9-141">The following transactions are supported:</span></span>

- <span data-ttu-id="6e4e9-142">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-142">Sales process</span></span>

    - <span data-ttu-id="6e4e9-143">ใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-143">Sales quotation</span></span>
    - <span data-ttu-id="6e4e9-144">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-144">Sales order</span></span>
    - <span data-ttu-id="6e4e9-145">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-145">Confirmation</span></span>
    - <span data-ttu-id="6e4e9-146">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e4e9-146">Picking list</span></span>
    - <span data-ttu-id="6e4e9-147">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-147">Packing slip</span></span>
    - <span data-ttu-id="6e4e9-148">ใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-148">Sales invoice</span></span>
    - <span data-ttu-id="6e4e9-149">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="6e4e9-149">Credit note</span></span>
    - <span data-ttu-id="6e4e9-150">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e4e9-150">Return order</span></span>
    - <span data-ttu-id="6e4e9-151">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6e4e9-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6e4e9-152">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="6e4e9-153">กระบวนการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-153">Purchase process</span></span>

    - <span data-ttu-id="6e4e9-154">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-154">Purchase order</span></span>
    - <span data-ttu-id="6e4e9-155">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-155">Confirmation</span></span>
    - <span data-ttu-id="6e4e9-156">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e4e9-156">Receipts list</span></span>
    - <span data-ttu-id="6e4e9-157">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e4e9-157">Product receipt</span></span>
    - <span data-ttu-id="6e4e9-158">ใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-158">Purchase invoice</span></span>
    - <span data-ttu-id="6e4e9-159">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="6e4e9-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="6e4e9-160">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="6e4e9-161">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="6e4e9-161">Credit note</span></span>
    - <span data-ttu-id="6e4e9-162">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="6e4e9-162">Return order</span></span>
    - <span data-ttu-id="6e4e9-163">ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-163">Purchase requisition</span></span>
    - <span data-ttu-id="6e4e9-164">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="6e4e9-165">คำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6e4e9-165">Request for quotation</span></span>
    - <span data-ttu-id="6e4e9-166">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัวของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6e4e9-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="6e4e9-167">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="6e4e9-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="6e4e9-168">กระบวนการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-168">Inventory process</span></span>

    - <span data-ttu-id="6e4e9-169">ใบสั่งโอนย้าย – จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-169">Transfer order – ship</span></span>
    - <span data-ttu-id="6e4e9-170">ใบสั่งโอนย้าย – รับ</span><span class="sxs-lookup"><span data-stu-id="6e4e9-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="6e4e9-171">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="6e4e9-171">Related resources</span></span>

[<span data-ttu-id="6e4e9-172">เริ่มต้นใช้งานบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="6e4e9-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="6e4e9-173">หมายเลขทะเบียน VAT หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="6e4e9-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="6e4e9-174">การสนับสนุนคุณลักษณะภาษีสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="6e4e9-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="6e4e9-175">วิธีการสร้างส่วนขยายในบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="6e4e9-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
