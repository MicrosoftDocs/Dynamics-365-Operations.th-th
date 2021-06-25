---
title: การคำนวณภาษี (พรีวิว)
description: หัวข้อนี้อธิบายขอบเขตและคุณลักษณะโดยรวมของความสามารถคํานวณภาษี
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184112"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="cfeda-103">การคำนวณภาษี (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="cfeda-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="cfeda-104">การคํานวณภาษีคือบริการเช่าแบบไฮเปอร์ซึ่งทำให้ Global Tax Engine เป็นแบบอัตโนมัติ และทำให้กระบวนการในการกำหนดและการคำนวณภาษีง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="cfeda-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="cfeda-105">กลไกจัดการภาษีสามารถตั้งค่าคอนฟิกได้อย่างสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="cfeda-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="cfeda-106">องค์ประกอบที่สามารถตั้งค่าคอนฟิกได้รวมถึง แต่ไม่จํากัดต่อ รูปแบบข้อมูลที่ต้องเสียภาษี รหัสภาษี เมทริกซ์การใช้งานภาษี และสูตรการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="cfeda-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="cfeda-107">กลไกจัดการภาษีจะรันบนแพลตฟอร์มบริการหลัก Microsoft Azure และนำเสนอเทคโนโลยีสมัยใหม่และความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="cfeda-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="cfeda-108">การคํานวณภาษีรวมกับ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cfeda-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cfeda-109">ในที่สุด จะยังรวมกับ Dynamics 365 Project Operations และ Dynamics 365 Commerce และแอปพลิเคชันอื่นๆ ของบุคคลที่หนึ่งและบุคคลที่สามด้วย</span><span class="sxs-lookup"><span data-stu-id="cfeda-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfeda-110">เมื่อคุณเปิดใช้งานบริการคํานวณภาษี การดําเนินงานบางอย่างในข้อมูลที่เกี่ยวข้องอาจดําเนินการในแหล่งข้อมูลอื่นที่ไม่ใช่ศูนย์กลางข้อมูลที่เก็บรักษาข้อมูลบริการของคุณ</span><span class="sxs-lookup"><span data-stu-id="cfeda-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="cfeda-111">ทบทวน [ข้อตกลงและเงื่อนไข](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) ก่อนที่จะเปิดใช้งานบริการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="cfeda-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="cfeda-112">การรักษาความเป็นส่วนตัวของคุณเป็นสิ่งสำคัญสำหรับเรา</span><span class="sxs-lookup"><span data-stu-id="cfeda-112">Your privacy is important to us.</span></span> <span data-ttu-id="cfeda-113">เรียนรู้เพิ่มเติม อ่าน [คำชี้แจงสิทธิส่วนบุคคล](https://go.microsoft.com/fwlink/?LinkId=521839) ของเรา</span><span class="sxs-lookup"><span data-stu-id="cfeda-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="cfeda-114">การคํานวณภาษีคือกลไกจัดการภาษีที่ใช้ไมโครเซอร์วิสที่นำเสนอความสามารถในการขยายแบบเลขชี้กำลัง</span><span class="sxs-lookup"><span data-stu-id="cfeda-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="cfeda-115">ซึ่งสามารถช่วยคุณในการดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cfeda-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="cfeda-116">ตั้งค่าคอนฟิกการคํานวณภาษีผ่าน Regulatory Configuration Service (RCS)</span><span class="sxs-lookup"><span data-stu-id="cfeda-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="cfeda-117">RCS เป็นรุ่นขั้นสูงของโปรแกรมออกแบบการรายงานทางอิเล็กทรอนิกส์ (ER) และพร้อมใช้งานในฐานะบริการแบบสแตนด์อโลน</span><span class="sxs-lookup"><span data-stu-id="cfeda-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="cfeda-118">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดรหัสและอัตราภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cfeda-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="cfeda-119">ตั้งค่าคอนฟิกเมทริกซ์ภาษีเพื่อกําหนดหมายเลขทะเบียนภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cfeda-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="cfeda-120">ตั้งค่าคอนฟิกโปรแกรมออกแบบการคํานวณภาษี เพื่อกําหนดสูตรและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="cfeda-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="cfeda-121">ใช้โซลูชันการกําหนดและการคํานวณภาษีระหว่างนิติบุคคลร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="cfeda-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="cfeda-122">หากต้องการใช้บริการคํานวณภาษี ให้ติดตั้ง Add-in ของบริการคํานวณภาษีจากโครงการของคุณใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="cfeda-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="cfeda-123">จากนั้น ให้ดำเนินการตั้งค่าใน RCS เสร็จสิ้น และเปิดใช้งานบริการคํานวณภาษีใน Finance และ Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cfeda-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="cfeda-124">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [เริ่มต้นใช้งานบริการภาษี](./global-get-started-with-tax-calculation-service.md)</span><span class="sxs-lookup"><span data-stu-id="cfeda-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="cfeda-125">ความพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="cfeda-125">Availability</span></span>

<span data-ttu-id="cfeda-126">การคํานวณภาษีพร้อมใช้งานเฉพาะในสภาพแวดล้อม Sandbox และกับลูกค้าที่เลือกเท่านั้น โดยผ่านโปรแกรมพรีวิวสำหรับสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="cfeda-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="cfeda-127">ในที่สุด จะพร้อมใช้งานโดยทั่วไปให้แก่ลูกค้าและในสภาพแวดล้อมการผลิตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cfeda-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="cfeda-128">คุณลักษณะใหม่จะยังคงมีการจัดส่ง ดังนั้นตรวจสอบให้แน่ใจว่าคู่มือล่าสุดมักจะทราบเกี่ยวกับความครอบคลุมและขอบเขตของคุณลักษณะที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cfeda-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="cfeda-129">การคํานวณภาษีถูกปรับใช้ในภูมิศาสตร์ Azure ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfeda-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="cfeda-130">นอกจากนี้ ยังจะถูกปรับใช้กับภูมิศาสตร์ Azure เพิ่มเติม ตามความต้องการของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="cfeda-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="cfeda-131">สหรัฐ</span><span class="sxs-lookup"><span data-stu-id="cfeda-131">United States</span></span>
- <span data-ttu-id="cfeda-132">ยุโรป</span><span class="sxs-lookup"><span data-stu-id="cfeda-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="cfeda-133">การคํานวณภาษีไม่สนับสนุนการปรับใช้ในสถานที่ของ Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cfeda-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="cfeda-134">นอกจากนี้ ยังไม่สนับสนุนรุ่นก่อนหน้านี้ด้วย เช่น Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="cfeda-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="cfeda-135">จุดเด่นของคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="cfeda-135">Feature highlights</span></span>

- <span data-ttu-id="cfeda-136">เมทริกซ์ภาษีที่ตั้งค่าคอนฟิกได้เพื่อกําหนดและคํานวณภาษีโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="cfeda-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="cfeda-137">การสนับสนุนสำหรับหมายเลขทะเบียนภาษีหลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="cfeda-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="cfeda-138">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดและการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="cfeda-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="cfeda-139">การสนับสนุนใบสั่งโอนย้ายสำหรับการกําหนดหมายเลขทะเบียนภาษีหลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="cfeda-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="cfeda-140">ธุรกรรมที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="cfeda-140">Supported transactions</span></span>

<span data-ttu-id="cfeda-141">สามารถเปิดใช้งานการคํานวณภาษีได้โดยนิติบุคคลและธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cfeda-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="cfeda-142">มีการสนับสนุนธุรกรรมต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="cfeda-142">The following transactions are supported:</span></span>

- <span data-ttu-id="cfeda-143">กระบวนการขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-143">Sales process</span></span>

    - <span data-ttu-id="cfeda-144">ใบเสนอราคาขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-144">Sales quotation</span></span>
    - <span data-ttu-id="cfeda-145">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-145">Sales order</span></span>
    - <span data-ttu-id="cfeda-146">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-146">Confirmation</span></span>
    - <span data-ttu-id="cfeda-147">รายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="cfeda-147">Picking list</span></span>
    - <span data-ttu-id="cfeda-148">บันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cfeda-148">Packing slip</span></span>
    - <span data-ttu-id="cfeda-149">ใบแจ้งหนี้การขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-149">Sales invoice</span></span>
    - <span data-ttu-id="cfeda-150">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="cfeda-150">Credit note</span></span>
    - <span data-ttu-id="cfeda-151">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="cfeda-151">Return order</span></span>
    - <span data-ttu-id="cfeda-152">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="cfeda-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cfeda-153">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="cfeda-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="cfeda-154">กระบวนการซื้อ</span><span class="sxs-lookup"><span data-stu-id="cfeda-154">Purchase process</span></span>

    - <span data-ttu-id="cfeda-155">ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="cfeda-155">Purchase order</span></span>
    - <span data-ttu-id="cfeda-156">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cfeda-156">Confirmation</span></span>
    - <span data-ttu-id="cfeda-157">รายการรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="cfeda-157">Receipts list</span></span>
    - <span data-ttu-id="cfeda-158">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="cfeda-158">Product receipt</span></span>
    - <span data-ttu-id="cfeda-159">ใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="cfeda-159">Purchase invoice</span></span>
    - <span data-ttu-id="cfeda-160">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัว</span><span class="sxs-lookup"><span data-stu-id="cfeda-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="cfeda-161">ค่าธรรมเนียมเบ็ดเตล็ดของรายการ</span><span class="sxs-lookup"><span data-stu-id="cfeda-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="cfeda-162">ใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="cfeda-162">Credit note</span></span>
    - <span data-ttu-id="cfeda-163">ใบสั่งส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="cfeda-163">Return order</span></span>
    - <span data-ttu-id="cfeda-164">ใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cfeda-164">Purchase requisition</span></span>
    - <span data-ttu-id="cfeda-165">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของใบขอซื้อ</span><span class="sxs-lookup"><span data-stu-id="cfeda-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="cfeda-166">คำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="cfeda-166">Request for quotation</span></span>
    - <span data-ttu-id="cfeda-167">ค่าธรรมเนียมเบ็ดเตล็ดของส่วนหัวของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="cfeda-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="cfeda-168">ค่าธรรมเนียมเบ็ดเตล็ดของรายการของคำขอใบเสนอราคา</span><span class="sxs-lookup"><span data-stu-id="cfeda-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="cfeda-169">กระบวนการสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="cfeda-169">Inventory process</span></span>

    - <span data-ttu-id="cfeda-170">ใบสั่งโอนย้าย – จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="cfeda-170">Transfer order – ship</span></span>
    - <span data-ttu-id="cfeda-171">ใบสั่งโอนย้าย – รับ</span><span class="sxs-lookup"><span data-stu-id="cfeda-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="cfeda-172">ทรัพยากรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="cfeda-172">Related resources</span></span>

[<span data-ttu-id="cfeda-173">เริ่มต้นใช้งานบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="cfeda-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="cfeda-174">หมายเลขทะเบียน VAT หลายหมายเลข</span><span class="sxs-lookup"><span data-stu-id="cfeda-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="cfeda-175">การสนับสนุนคุณลักษณะภาษีสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="cfeda-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="cfeda-176">วิธีการสร้างส่วนขยายในบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="cfeda-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
