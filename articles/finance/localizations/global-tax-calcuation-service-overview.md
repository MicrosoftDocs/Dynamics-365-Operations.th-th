---
title: การคำนวณภาษี (พรีวิว)
description: หัวข้อนี้อธิบายขอบเขตและคุณลักษณะโดยรวมของความสามารถคํานวณภาษี
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892360"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="0265d-103">การคำนวณภาษี (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="0265d-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="0265d-104">การคํานวณภาษีคือบริการเช่าแบบไฮเปอร์ซึ่งทำให้ Global Tax Engine เป็นแบบอัตโนมัติ และทำให้กระบวนการในการกำหนดและการคำนวณภาษีง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="0265d-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="0265d-105">กลไกจัดการภาษีสามารถตั้งค่าคอนฟิกได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="0265d-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="0265d-106">องค์ประกอบที่สามารถตั้งค่าคอนฟิกได้รวมถึง แต่ไม่จํากัดต่อ รูปแบบข้อมูลที่ต้องเสียภาษี รหัสภาษี เมทริกซ์การใช้งานภาษี และสูตรการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="0265d-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="0265d-107">กลไกจัดการภาษีจะรันบนแพลตฟอร์มบริการหลัก Microsoft Azure และนำเสนอเทคโนโลยีสมัยใหม่และความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="0265d-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="0265d-108">การคํานวณภาษีรวมกับ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0265d-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0265d-109">ในที่สุด จะยังรวมกับ Dynamics 365 Project Operations และ Dynamics 365 Commerce และแอปพลิเคชันอื่นๆ ของบุคคลที่หนึ่งและบุคคลที่สามด้วย</span><span class="sxs-lookup"><span data-stu-id="0265d-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="0265d-110">การคํานวณภาษีคือกลไกจัดการภาษีที่ใช้ไมโครเซอร์วิสที่นำเสนอความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="0265d-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="0265d-111">ซึ่งสามารถช่วยคุณในการดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0265d-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="0265d-112">ตั้งค่าคอนฟิกการคํานวณภาษีผ่าน Regulatory Configuration Service (RCS)</span><span class="sxs-lookup"><span data-stu-id="0265d-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="0265d-113">RCS เป็นรุ่นขั้นสูงของโปรแกรมออกแบบการรายงานทางอิเล็กทรอนิกส์ (ER) และพร้อมใช้งานในฐานะบริการแบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="0265d-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="0265d-114">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดรหัสและอัตราภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0265d-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="0265d-115">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดหมายเลขทะเบียนภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0265d-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="0265d-116">ตั้งค่าคอนฟิกโปรแกรมออกแบบการคํานวณภาษี เพื่อกําหนดสูตรและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="0265d-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="0265d-117">ใช้โซลูชันการกําหนดและการคํานวณภาษีระหว่างนิติบุคคลร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="0265d-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="0265d-118">หากต้องการใช้บริการคํานวณภาษี ให้ติดตั้ง Add-in ของบริการคํานวณภาษีจากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="0265d-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0265d-119">จากนั้น ให้ดำเนินการตั้งค่าใน RCS เสร็จสิ้น และเปิดใช้งานบริการคํานวณภาษีใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0265d-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="0265d-120">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เริ่มต้นใช้งานบริการภาษี](./global-get-started-with-tax-calculation-service.md)</span><span class="sxs-lookup"><span data-stu-id="0265d-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="0265d-121">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0265d-121">Availability</span></span>

<span data-ttu-id="0265d-122">การคํานวณภาษีพร้อมใช้งานเฉพาะในสภาพแวดล้อม Sandbox และกับลูกค้าที่เลือกเท่านั้น โดยผ่านโปรแกรมพรีวิวสำหรับสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="0265d-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="0265d-123">ในที่สุด จะพร้อมใช้งานโดยทั่วไปให้แก่ลูกค้าและในสภาพแวดล้อมการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0265d-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="0265d-124">คุณลักษณะใหม่จะยังคงมีการจัดส่ง ดังนั้นตรวจสอบให้แน่ใจว่าคู่มือล่าสุดมักจะทราบเกี่ยวกับความครอบคลุมและขอบเขตของคุณลักษณะที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0265d-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="0265d-125">การคํานวณภาษีถูกปรับใช้ในภูมิศาสตร์ Azure ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0265d-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="0265d-126">นอกจากนี้ ยังจะถูกปรับใช้กับภูมิศาสตร์ Azure เพิ่มเติม ตามความต้องการของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="0265d-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="0265d-127">สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="0265d-127">United States</span></span>
- <span data-ttu-id="0265d-128">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="0265d-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="0265d-129">การคํานวณภาษีไม่สนับสนุนการปรับใช้ในสถานที่ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="0265d-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="0265d-130">นอกจากนี้ ยังไม่สนับสนุนรุ่นก่อนหน้านี้ด้วย เช่น Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="0265d-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="0265d-131">จุดเด่นของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="0265d-131">Feature highlights</span></span>

- <span data-ttu-id="0265d-132">เมทริกซ์ภาษีที่ตั้งค่าคอนฟิกได้เพื่อกําหนดและคํานวณภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0265d-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="0265d-133">การสนับสนุนสำหรับหมายเลขทะเบียนภาษีหลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0265d-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="0265d-134">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดและการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="0265d-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="0265d-135">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดหมายเลขทะเบียนภาษีหลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0265d-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="0265d-136">ธุรกรรมที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="0265d-136">Supported transactions</span></span>

<span data-ttu-id="0265d-137">สามารถเปิดใช้งานการคํานวณภาษีได้โดยนิติบุคคลและธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="0265d-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="0265d-138">มีการสนับสนุนธุรกรรมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0265d-138">The following transactions are supported:</span></span>

- <span data-ttu-id="0265d-139">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-139">Sales process</span></span>

    - <span data-ttu-id="0265d-140">ใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-140">Sales quotation</span></span>
    - <span data-ttu-id="0265d-141">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-141">Sales order</span></span>
    - <span data-ttu-id="0265d-142">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-142">Confirmation</span></span>
    - <span data-ttu-id="0265d-143">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="0265d-143">Picking list</span></span>
    - <span data-ttu-id="0265d-144">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0265d-144">Packing slip</span></span>
    - <span data-ttu-id="0265d-145">ใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-145">Sales invoice</span></span>
    - <span data-ttu-id="0265d-146">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0265d-146">Credit note</span></span>
    - <span data-ttu-id="0265d-147">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0265d-147">Return order</span></span>
    - <span data-ttu-id="0265d-148">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="0265d-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="0265d-149">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="0265d-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="0265d-150">กระบวนการซื้อ</span><span class="sxs-lookup"><span data-stu-id="0265d-150">Purchase process</span></span>

    - <span data-ttu-id="0265d-151">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="0265d-151">Purchase order</span></span>
    - <span data-ttu-id="0265d-152">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="0265d-152">Confirmation</span></span>
    - <span data-ttu-id="0265d-153">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0265d-153">Receipts list</span></span>
    - <span data-ttu-id="0265d-154">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0265d-154">Product receipt</span></span>
    - <span data-ttu-id="0265d-155">ใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="0265d-155">Purchase invoice</span></span>
    - <span data-ttu-id="0265d-156">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="0265d-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="0265d-157">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="0265d-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="0265d-158">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0265d-158">Credit note</span></span>
    - <span data-ttu-id="0265d-159">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="0265d-159">Return order</span></span>
    - <span data-ttu-id="0265d-160">ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="0265d-160">Purchase requisition</span></span>
    - <span data-ttu-id="0265d-161">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="0265d-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="0265d-162">คำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0265d-162">Request for quotation</span></span>
    - <span data-ttu-id="0265d-163">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัวของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0265d-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="0265d-164">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="0265d-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="0265d-165">กระบวนการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="0265d-165">Inventory process</span></span>

    - <span data-ttu-id="0265d-166">ใบสั่งโอนย้าย – จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0265d-166">Transfer order – ship</span></span>
    - <span data-ttu-id="0265d-167">ใบสั่งโอนย้าย – รับ</span><span class="sxs-lookup"><span data-stu-id="0265d-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="0265d-168">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0265d-168">Related resources</span></span>

[<span data-ttu-id="0265d-169">เริ่มต้นใช้งานบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="0265d-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="0265d-170">หมายเลขทะเบียน VAT หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="0265d-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="0265d-171">การสนับสนุนคุณลักษณะภาษีสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="0265d-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="0265d-172">วิธีการสร้างส่วนขยายในบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="0265d-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)