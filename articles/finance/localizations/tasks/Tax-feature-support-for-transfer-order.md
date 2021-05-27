---
title: การสนับสนุนคุณลักษณะภาษีสำหรับใบสั่งโอนย้าย
description: หัวข้อนี้อธิบายการสนับสนุนคุณลักษณะภาษีใหม่สำหรับใบสั่งโอนย้าย โดยใช้บริการคํานวณภาษี
author: kailiang
ms.date: 04/20/2021
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
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021380"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="948e8-103">การสนับสนุนคุณลักษณะภาษีสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="948e8-104">หัวข้อนี้แสดงข้อมูลเกี่ยวกับการคํานวณภาษีและการรวมการลงรายการบัญชีในใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="948e8-105">ฟังก์ชันนี้ช่วยให้คุณสามารถตั้งค่าการคํานวณภาษีและการลงรายการบัญชีในใบสั่งโอนย้ายเพื่อการโอนย้ายสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="948e8-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="948e8-106">ภายใต้ข้อบังคับภาษีมูลค่าเพิ่ม (VAT) ของสหภาพยุโรป (EU) การโอนย้ายสินค้าคงคลังจะถือเป็นวัสดุแบบ intra-community และการซื้อแบบ intra-community</span><span class="sxs-lookup"><span data-stu-id="948e8-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="948e8-107">เมื่อต้องการตั้งค่าคอนฟิกและใช้ฟังก์ชันนี้ คุณต้องปฏิบัติตามขั้นตอนหลักสามขั้นตอน:</span><span class="sxs-lookup"><span data-stu-id="948e8-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="948e8-108">**การตั้งค่า RCS:** ใน Regulatory Configuration Service ให้ตั้งค่าคุณลักษณะภาษี รหัสภาษี และการใช้งานรหัสภาษี สำหรับการกําหนดรหัสภาษีในใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="948e8-109">**การตั้งค่า Finance:** ใน Microsoft Dynamics 365 Finance ให้เปิดคุณลักษณะ **ภาษีในใบสั่งโอนย้าย** ตั้งค่าพารามิเตอร์บริการภาษีสำหรับสินค้าคงคลัง และตั้งค่าพารามิเตอร์ภาษีหลัก</span><span class="sxs-lookup"><span data-stu-id="948e8-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="948e8-110">**การตั้งค่าสินค้าคงคลัง:** ตั้งค่าการตั้งค่าคอนฟิกสินค้าคงคลังสำหรับธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="948e8-111">ตั้งค่า RCS สำหรับธุรกรรมภาษีและใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="948e8-112">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าภาษีที่เกี่ยวข้องในใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="948e8-113">ในตัวอย่างที่แสดงที่นี่ ใบสั่งโอนย้ายมาจากเนเธอร์แลนด์ไปยังเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="948e8-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="948e8-114">บนหน้า **คุณลักษณะภาษี** บนแท็บ **รุ่น** ให้เลือกรุ่นคุณลักษณะแบบร่าง แล้วจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="948e8-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![การเลือกแก้ไข](../media/tax-feature-support-01.png)

2. <span data-ttu-id="948e8-116">บนหน้า **การตั้งค่าคุณลักษณะภาษี** บนแท็บ **รหัสภาษี** ให้เลือก **เพิ่ม** เพื่อสร้างรหัสภาษีใหม่</span><span class="sxs-lookup"><span data-stu-id="948e8-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="948e8-117">สำหรับตัวอย่างนี้ มีการสร้างรหัสภาษีสามรหัส: **NL-Exempt**, **BE-RC-21** และ **BE-RC+21**</span><span class="sxs-lookup"><span data-stu-id="948e8-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="948e8-118">เมื่อใบสั่งโอนย้ายถูกจัดส่งจากคลังสินค้าในเนเธอร์แลนด์ มีการใช้รหัสภาษีที่ได้รับยกเว้น VAT ของเนเธอร์แลนด์ (**NL-Exempt**)</span><span class="sxs-lookup"><span data-stu-id="948e8-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="948e8-119">สร้างรหัสภาษี **NL-Exempt**</span><span class="sxs-lookup"><span data-stu-id="948e8-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="948e8-120">เลือก **เพิ่ม** ป้อน **NL-Exempt** ในฟิลด์ **รหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="948e8-121">เลือก **ตามยอดเงินสุทธิ** ในฟิลด์ **ส่วนประกอบภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="948e8-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="948e8-122">Select **Save**.</span></span>
        4. <span data-ttu-id="948e8-123">เลือก **เพิ่ม** ในตาราง **อัตรา**</span><span class="sxs-lookup"><span data-stu-id="948e8-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="948e8-124">สลับ **ได้รับยกเว้น** เป็น **ใช่** ในส่วน **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="948e8-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![รหัสภาษี NL-Exempt](../media/tax-feature-support-02.png)

    - <span data-ttu-id="948e8-126">เมื่อได้รับใบสั่งโอนย้ายที่คลังสินค้าของเบลเยียม จะมีการใช้ระบบการเก็บภาษีย้อนกลับโดยใช้รหัสภาษี **BE-RC-21** และ **BE-RC+21**</span><span class="sxs-lookup"><span data-stu-id="948e8-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="948e8-127">สร้างรหัสภาษี **BE-RC-21**</span><span class="sxs-lookup"><span data-stu-id="948e8-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="948e8-128">เลือก **เพิ่ม** ป้อน **BE-RC-21** ในฟิลด์ **รหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="948e8-129">เลือก **ตามยอดเงินสุทธิ** ในฟิลด์ **ส่วนประกอบภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="948e8-130">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="948e8-130">Select **Save**.</span></span>
        4. <span data-ttu-id="948e8-131">เลือก **เพิ่ม** ในตาราง **อัตรา**</span><span class="sxs-lookup"><span data-stu-id="948e8-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="948e8-132">ป้อน **-21** ในฟิลด์ **อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="948e8-133">สลับ **เป็นการเก็บภาษีย้อนกลับ** เป็น **ใช่** ในส่วน **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="948e8-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="948e8-134">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="948e8-134">Select **Save**.</span></span>

        ![รหัสภาษี BE-RC-21 สำหรับการเก็บภาษีย้อนกลับ](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="948e8-136">สร้างรหัสภาษี **BE-RC+21**</span><span class="sxs-lookup"><span data-stu-id="948e8-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="948e8-137">เลือก **เพิ่ม** ป้อน **BE-RC-21** ในฟิลด์ **รหัสภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="948e8-138">เลือก **ตามยอดเงินสุทธิ** ในฟิลด์ **ส่วนประกอบภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="948e8-139">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="948e8-139">Select **Save**.</span></span>
        4. <span data-ttu-id="948e8-140">เลือก **เพิ่ม** ในตาราง **อัตรา**</span><span class="sxs-lookup"><span data-stu-id="948e8-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="948e8-141">ป้อน **21** ในฟิลด์ **อัตราภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="948e8-142">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="948e8-142">Select **Save**.</span></span>

        ![รหัสภาษี BE-RC+21 สำหรับการเก็บภาษีย้อนกลับ](../media/tax-feature-support-04.png)

3. <span data-ttu-id="948e8-144">กําหนดการใช้งานของรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="948e8-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="948e8-145">เลือก **จัดการคอลัมน์** แล้วจากนั้น เลือกคอลัมน์ที่ควรใช้ในการสร้างตารางการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="948e8-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="948e8-146">ตรวจสอบให้แน่ใจว่าได้เพิ่มคอลัมน์ **กระบวนการทางธุรกิจ** และ **ทิศทางภาษี** ลงในตาราง</span><span class="sxs-lookup"><span data-stu-id="948e8-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="948e8-147">ทั้งสองคอลัมน์เป็นข้อมูลพื้นฐานสำหรับฟังก์ชันสำหรับภาษีในใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="948e8-148">เพิ่มกฎการนำไปใช้ได้</span><span class="sxs-lookup"><span data-stu-id="948e8-148">Add applicability rules.</span></span> <span data-ttu-id="948e8-149">อย่าปล่อยฟิลด์ **รหัสภาษี** **กลุ่มภาษี** และ **กลุ่มภาษีสินค้า** ให้ว่าง</span><span class="sxs-lookup"><span data-stu-id="948e8-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="948e8-150">เพิ่มกฎใหม่สำหรับการจัดส่งใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="948e8-151">เลือก **เพิ่ม** ในตาราง **กฎการนำไปใช้ได้**</span><span class="sxs-lookup"><span data-stu-id="948e8-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="948e8-152">ในฟิลด์ **กระบวนการทางธุรกิจ** ให้เลือก **สินค้าคงคลัง** เพื่อทำให้กฎนั้นใช้ได้สำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="948e8-153">ในฟิลด์ **จัดส่งจากประเทศ/ภูมิภาค** ให้ป้อน **NLD**</span><span class="sxs-lookup"><span data-stu-id="948e8-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="948e8-154">ในฟิลด์ **จัดส่งไปยังประเทศ/ภูมิภาค** ให้ป้อน **BEL**</span><span class="sxs-lookup"><span data-stu-id="948e8-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="948e8-155">ในฟิลด์ **ทิศทางภาษี** ให้เลือก **ผลลัพธ์** เพื่อทำให้กฎใช้ได้กับการจัดส่งใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="948e8-156">ในฟิลด์ **รหัสภาษี** เลือก **NL-Exempt**</span><span class="sxs-lookup"><span data-stu-id="948e8-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="948e8-157">ในฟิลด์ **กลุ่มภาษี** และ **กลุ่มภาษีสินค้า** ให้ป้อนกลุ่มภาษีขายที่เกี่ยวข้องและกลุ่มภาษีขายตามประเภทสินค้าซึ่งกําหนดไว้ในระบบ Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="948e8-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="948e8-158">เพิ่มอีกกฎหนึ่งสำหรับการรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="948e8-159">เลือก **เพิ่ม** ในตาราง **กฎการนำไปใช้ได้**</span><span class="sxs-lookup"><span data-stu-id="948e8-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="948e8-160">ในฟิลด์ **กระบวนการทางธุรกิจ** ให้เลือก **สินค้าคงคลัง** เพื่อทำให้กฎนั้นใช้ได้สำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="948e8-161">ในฟิลด์ **จัดส่งจากประเทศ/ภูมิภาค** ให้ป้อน **NLD**</span><span class="sxs-lookup"><span data-stu-id="948e8-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="948e8-162">ในฟิลด์ **จัดส่งไปยังประเทศ/ภูมิภาค** ให้ป้อน **BEL**</span><span class="sxs-lookup"><span data-stu-id="948e8-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="948e8-163">ในฟิลด์ **ทิศทางภาษี** ให้เลือก **อินพุต** เพื่อทำให้กฎใช้ได้กับการรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="948e8-164">ในฟิลด์ **รหัสภาษี** ให้เลือก **BE-RC+21** และ **BE-RC-21**</span><span class="sxs-lookup"><span data-stu-id="948e8-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="948e8-165">ในฟิลด์ **กลุ่มภาษี** และ **กลุ่มภาษีสินค้า** ให้ป้อนกลุ่มภาษีขายที่เกี่ยวข้องและกลุ่มภาษีขายตามประเภทสินค้าซึ่งกําหนดไว้ในระบบ Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="948e8-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![กฎการนำไปใช้ได้](../media/image5.png)

4. <span data-ttu-id="948e8-167">กรอกข้อมูลและเผยแพร่รุ่นของคุณลักษณะภาษีใหม่</span><span class="sxs-lookup"><span data-stu-id="948e8-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="948e8-168">[![การเปลี่ยนสถานะของรุ่นใหม่](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="948e8-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="948e8-169">ตั้งค่า Finance สำหรับธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="948e8-170">ให้ทำตามขั้นตอนเหล่านี้เพื่อเปิดใช้งานและตั้งค่าภาษีสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="948e8-171">ใน Finance ไปที่ **พื้นที่ทำงาน** \> **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="948e8-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="948e8-172">ในรายการ ให้ค้นหาและเลือกคุณลักษณะ **ภาษีในใบสั่งโอนย้าย** แล้วจากนั้น เลือก **เปิดใช้งานทันที** เพื่อเปิด</span><span class="sxs-lookup"><span data-stu-id="948e8-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="948e8-173">คุณลักษณะ **ภาษีในใบสั่งโอนย้าย** ขึ้นอยู่กับบริการภาษีทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="948e8-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="948e8-174">ดังนั้น จึงสามารถเปิดใช้งานได้เฉพาะหลังจากที่คุณติดตั้งบริการภาษีแล้วเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="948e8-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![คุณลักษณะภาษีในใบสั่งโอนย้าย](../media/image7.png)

3. <span data-ttu-id="948e8-176">เปิดใช้งานบริการภาษี และเลือกกระบวนการทางธุรกิจของ **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="948e8-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="948e8-177">คุณต้องดำเนินการขั้นตอนนี้ให้ครบถ้วนสำหรับนิติบุคคลแต่ละแห่งใน Finance ที่ซึ่งคุณต้องการให้บริการภาษีและฟังก์ชันสำหรับภาษีในใบสั่งโอนย้ายพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="948e8-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="948e8-178">ไปที่ **ภาษี** \> **การตั้งค่า** \> **การตั้งค่าคอนฟิกภาษี** \> **การตั้งค่าบริการภาษี**</span><span class="sxs-lookup"><span data-stu-id="948e8-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="948e8-179">ในฟิลด์ **กระบวนการทางธุรกิจ** ให้เลือก **สินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="948e8-179">In the **Business process** field, select **Inventory**.</span></span>

    ![การตั้งค่าฟิลด์กระบวนการทางธุรกิจ](../media/image8.png)

4. <span data-ttu-id="948e8-181">ตรวจสอบว่ามีการตั้งค่าระบบการเก็บภาษีย้อนกลับแล้ว</span><span class="sxs-lookup"><span data-stu-id="948e8-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="948e8-182">ไปที่ **บัญชีแยกประเภททั่วไป** \> **การตั้งค่า** \> **พารามิเตอร์** แล้วจากนั้น บนแท็บ **การเก็บภาษีย้อนกลับ** ให้ตรวจสอบว่าตัวเลือก **เปิดใช้งานการเก็บภาษีย้อนกลับ** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="948e8-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![เปิดใช้งานตัวเลือกการเก็บภาษีย้อนกลับ](../media/image9.png)

5. <span data-ttu-id="948e8-184">ตรวจสอบว่ามีการตั้งค่ารหัสภาษี กลุ่มภาษี กลุ่มภาษีสินค้า และหมายเลขทะเบียน VAT ที่เกี่ยวข้องใน Finance ตามคำแนะนำบริการภาษี</span><span class="sxs-lookup"><span data-stu-id="948e8-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="948e8-185">ตั้งค่าบัญชีการส่งต่อระหว่างกาล</span><span class="sxs-lookup"><span data-stu-id="948e8-185">Set up an interim transit account.</span></span> <span data-ttu-id="948e8-186">ต้องใช้ขั้นตอนนี้เฉพาะเมื่อภาษีที่ใช้กับใบสั่งโอนย้าย ไม่สามารถใช้ได้กับระบบที่ได้รับยกเว้นภาษีหรือระบบการเก็บภาษีย้อนกลับ</span><span class="sxs-lookup"><span data-stu-id="948e8-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="948e8-187">ไปที่ **ภาษี** \> **การตั้งค่า** \> **ภาษีขาย** \> **กลุ่มการลงรายการบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="948e8-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="948e8-188">ในฟิลด์ **การส่งต่อระหว่างกาล** ให้เลือกบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="948e8-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![การเลือกบัญชีการส่งต่อระหว่างกาล](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="948e8-190">ตั้งค่าสินค้าคงคลังพื้นฐานสำหรับธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="948e8-191">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าสินค้าคงคลังพื้นฐานเพื่อเปิดใช้งานธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="948e8-192">สร้างไซต์จัดส่งจากและจัดส่งไปยังสำหรับคลังสินค้าของคุณในประเทศหรือภูมิภาคต่างๆ และเพิ่มที่อยู่หลักสำหรับแต่ละไซต์</span><span class="sxs-lookup"><span data-stu-id="948e8-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="948e8-193">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **คลังสินค้า** \> **ไซต์**</span><span class="sxs-lookup"><span data-stu-id="948e8-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="948e8-194">เลือก **สร้าง** เพื่อสร้างไซต์ที่คุณจะกําหนดให้กับคลังสินค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="948e8-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="948e8-195">ทำซ้ำขั้นตอนที่ 2 สำหรับไซต์อื่นๆ ทั้งหมดที่คุณต้องสร้าง</span><span class="sxs-lookup"><span data-stu-id="948e8-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="948e8-196">หนึ่งในไซต์ที่คุณสร้างขึ้นควรมีชื่อว่า **ส่งต่อ**</span><span class="sxs-lookup"><span data-stu-id="948e8-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="948e8-197">ในขั้นตอนต่อมาของกระบวนงานนี้ คุณจะกําหนดไซต์นี้ให้กับคลังสินค้าส่งต่อ เพื่อให้สามารถลงรายการบัญชีใบสำคัญสินค้าคงคลังที่เกี่ยวข้องกับภาษีในธุรกรรม "จัดส่ง" และ "รับสินค้า" สำหรับใบสั่งโอนย้ายได้</span><span class="sxs-lookup"><span data-stu-id="948e8-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="948e8-198">ที่อยู่ของไซต์การส่งต่อไม่เกี่ยวข้องกับการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="948e8-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="948e8-199">ดังนั้น คุณสามารถปล่อยให้ว่างได้</span><span class="sxs-lookup"><span data-stu-id="948e8-199">Therefore, you can leave it blank.</span></span>

    ![การตั้งค่าไซต์](../media/image11.png)

2. <span data-ttu-id="948e8-201">สร้างคลังสินค้าที่จัดส่งจาก ส่งต่อ และจัดส่งไปยัง</span><span class="sxs-lookup"><span data-stu-id="948e8-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="948e8-202">ข้อมูลที่อยู่ใดๆ ที่เก็บรักษาอยู่ในคลังสินค้า จะแทนที่ที่อยู่ไซต์ในระหว่างการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="948e8-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="948e8-203">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **คลังสินค้า** \> **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="948e8-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="948e8-204">เลือก **สร้าง** เพื่อสร้างคลังสินค้า และกําหนดให้กับไซต์ที่เกี่ยวข้องในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="948e8-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="948e8-205">ทําซ้ำขั้นตอนที่ 2 เพื่อสร้างคลังสินค้าสำหรับแต่ละไซต์ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="948e8-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![การตั้งค่าคลังสินค้า](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="948e8-207">สำหรับคลังสินค้าจัดส่งจาก คุณต้องเลือกคลังสินค้าส่งต่อในฟิลด์ **คลังสินค้าส่งต่อ** สำหรับธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![การเลือกคลังสินค้าส่งต่อ](../media/image13.png)

3. <span data-ttu-id="948e8-209">ตรวจสอบว่ามีการตั้งค่าการตั้งค่าคอนฟิกการลงรายการบัญชีสินค้าคงคลังสำหรับธุรกรรมใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="948e8-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="948e8-210">ไปที่ **การจัดการสินค้างคงคลัง** \> **การตั้งค่า** \> **การลงรายการบัญชี** \> **การลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="948e8-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="948e8-211">บนแท็บ **สินค้าคงคลัง** ให้ตรวจสอบว่ามีการตั้งค่าบัญชีแยกประเภทไว้สำหรับทั้งการลงรายการบัญชี **การออกสินค้าคงคลัง** และ **การรับสต็อก**</span><span class="sxs-lookup"><span data-stu-id="948e8-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![การตั้งค่าการลงรายการบัญชีการออกใช้สินค้าคงคลังและการรับสต็อก](../media/image14.png)

    3. <span data-ttu-id="948e8-213">ตรวจสอบว่ามีการตั้งค่าบัญชีแยกประเภทสำหรับการลงรายการบัญชี **เจ้าหนี้ระหว่างหน่วย**</span><span class="sxs-lookup"><span data-stu-id="948e8-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![การตั้งค่าการลงรายการบัญชีเจ้าหนี้ระหว่างหน่วย](../media/image15.png)

    4. <span data-ttu-id="948e8-215">ตรวจสอบว่ามีการตั้งค่าบัญชีแยกประเภทสำหรับการลงรายการบัญชี **ลูกหนี้ระหว่างหน่วย**</span><span class="sxs-lookup"><span data-stu-id="948e8-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![การตั้งค่าการลงรายการบัญชีลูกหนี้ระหว่างหน่วย](../media/image16.png)
