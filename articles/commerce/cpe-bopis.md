---
title: ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมิน Dynamics 365 Commerce
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกการซื้อออนไลน์ การเบิกสินค้าในร้านค้า (BOPIS) ในสภาพแวดล้อมการประเมิน Microsoft Dynamics 365 Commerce หลังจากที่มีการเตรียมใช้งาน
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416026"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="39b1d-103">ตั้งค่าคอนฟิก BOPIS ในสภาพแวดล้อมการประเมิน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39b1d-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกการซื้อออนไลน์ การเบิกสินค้าในร้านค้า (BOPIS) ในสภาพแวดล้อมการประเมิน Microsoft Dynamics 365 Commerce หลังจากที่มีการเตรียมใช้งานสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="39b1d-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="39b1d-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="39b1d-105">Prerequisite</span></span>

<span data-ttu-id="39b1d-106">ทำตามกระบวนงานในหัวข้อนี้ให้เสร็จสมบูรณ์ เฉพาะหลังจากที่มีการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อมการประเมิน Commerce ของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="39b1d-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="39b1d-107">สำหรับข้อมูลเกี่ยวกับวิธีการเตรียมใช้งานและตั้งค่าคอนฟิกสภาพแวดล้อมของคุณ ให้ดูที่ [เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](provisioning-guide.md) และ [ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning)</span><span class="sxs-lookup"><span data-stu-id="39b1d-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="39b1d-108">หลังจากที่มีการเตรียมใช้งานและการตั้งค่าคอนฟิกสภาพแวดล้อม Commerce ของคุณตั้งแต่ต้นจนจบ คุณสามารถใช้หัวข้อนี้เพื่อเปิดใช้งานสถานการณ์จำลอง BOPIS</span><span class="sxs-lookup"><span data-stu-id="39b1d-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="39b1d-109">ตั้งค่าคอนฟิก POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="39b1d-110">ตั้งค่าคอนฟิก Modern POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-110">Configure Modern POS</span></span>

<span data-ttu-id="39b1d-111">สถานการณ์จำลอง BOPIS ที่เกี่ยวข้องกับการชำระเงินด้วยบัตรเครดิต ต้องมีสถานีฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="39b1d-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="39b1d-112">สถานีฮาร์ดแวร์ถูกสร้างขึ้นในไคลเอนต์ Modern POS for Windows และ Android</span><span class="sxs-lookup"><span data-stu-id="39b1d-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="39b1d-113">ถ้าคุณกำลังใช้ Cloud POS หรือ Modern POS สำหรับ iOS ไคลเอนต์การขายหน้าร้าน (POS) ต้องมีการจับคู่กับสถานีฮาร์ดแวร์ที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="39b1d-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="39b1d-114">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิก BOPIS สำหรับ Windows และไคลเอนต์ Android</span><span class="sxs-lookup"><span data-stu-id="39b1d-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="39b1d-115">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าสถานีฮาร์ดแวร์ที่ใช้ร่วมกัน ให้ดู [ตั้งค่าคอนฟิกและติดตั้งสถานีฮาร์ดแวร์ Retail](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation)</span><span class="sxs-lookup"><span data-stu-id="39b1d-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="39b1d-116">ไปยัง **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> เครื่องบันทึกเงินสด**</span><span class="sxs-lookup"><span data-stu-id="39b1d-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="39b1d-117">เลือกลงทะเบียน **SANFRAN-5** แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="39b1d-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="39b1d-118">เปลี่ยนค่าของฟิลด์ **โพรไฟล์ฮาร์ดแวร์** จาก **HW002** เป็น **HW001** แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="39b1d-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="39b1d-119">เพื่อซิงโครไนส์การเปลี่ยนแปลง ไปที่ **Retail และ Commerce \> Retail และ Commerce IT \> กำหนดการกระจาย**</span><span class="sxs-lookup"><span data-stu-id="39b1d-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="39b1d-120">เลือกกำหนดการกระจาย **1090** และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **เรียกใช้เดี๋ยวนี้**</span><span class="sxs-lookup"><span data-stu-id="39b1d-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="39b1d-121">เลือก **ใช่** แล้วจากนั้น **ตกลง** เพื่อเริ่มการซิงโครไนส์ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="39b1d-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="39b1d-122">ติดตั้ง Modern POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-122">Install Modern POS</span></span>

1. <span data-ttu-id="39b1d-123">ไปยัง **Retail และ Commerce \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> อุปกรณ์**</span><span class="sxs-lookup"><span data-stu-id="39b1d-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="39b1d-124">เลือกอุปกรณ์ **SANFRANCIS-5**</span><span class="sxs-lookup"><span data-stu-id="39b1d-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="39b1d-125">บนบานหน้าต่างการดำเนินการ เลือก **ดาวน์โหลด** และจากนั้นเลือก **ไฟล์การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="39b1d-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="39b1d-126">เลือก **ดาวน์โหลด** แล้วเลือก **Retail Modern POS**</span><span class="sxs-lookup"><span data-stu-id="39b1d-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="39b1d-127">เมื่อการดาวน์โหลดของไฟล์ **ModernPOSSetup.exe** เสร็จสมบูรณ์ ให้เลือก **เปิดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="39b1d-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![เปิดไฟล์](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="39b1d-129">เลือก **ถัดไป** เพื่อไปยังกระบวนการติดตั้ง</span><span class="sxs-lookup"><span data-stu-id="39b1d-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="39b1d-130">เมื่อการติดตั้งเสร็จสมบูรณ์ ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="39b1d-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="39b1d-131">เรียกใช้งาน Modern POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-131">Activate Modern POS</span></span>

1. <span data-ttu-id="39b1d-132">บนเดสก์ท็อป Windows ให้เลือกปุ่ม **เริ่มต้น** แล้วป้อน **Retail Modern POS**</span><span class="sxs-lookup"><span data-stu-id="39b1d-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="39b1d-133">เลือกแอพลิเคชัน **Retail Modern POS** เพื่อเริ่มต้นการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="39b1d-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="39b1d-134">เลือก **ถัดไป**</span><span class="sxs-lookup"><span data-stu-id="39b1d-134">Select **Next**.</span></span> <span data-ttu-id="39b1d-135">ฟิลด์ **URL ของเซิร์ฟเวอร์** **รหัสอุปกรณ์** และ **หมายเลขเครื่องบันทึกเงินสด** ควรถูกกำหนดไว้ล่วงหน้าโดยใช้ข้อมูลจากไฟล์การตั้งค่าคอนฟิกที่คุณดาวน์โหลดไว้ในกระบวนงานก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="39b1d-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="39b1d-136">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="39b1d-136">Select **Activate**.</span></span>
5. <span data-ttu-id="39b1d-137">กล่องโต้ตอบการรับรองความถูกต้องจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="39b1d-137">An authentication dialog box appears.</span></span> <span data-ttu-id="39b1d-138">เลือกบัญชีที่ใช้ที่อยู่อีเมลที่เกี่ยวข้องก่อนหน้านี้กับผู้ปฏิบัติงาน **000713 - Andrew Collette**</span><span class="sxs-lookup"><span data-stu-id="39b1d-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="39b1d-139">ถ้าคุณยังไม่ได้เชื่อมโยงผู้ปฏิบัติงานกับข้อมูลประจำตัวของคุณ การเรียกใช้งานจะไม่ประสบความสำเร็จ</span><span class="sxs-lookup"><span data-stu-id="39b1d-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="39b1d-140">ในกรณีนี้ ให้ทำตามขั้นตอนภายใต้ส่วน "เชื่อมโยงผู้ปฏิบัติงานกับรหัสประจำตัวของคุณ" ในหัวข้อ [ตั้งค่าคอนฟิกสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity)</span><span class="sxs-lookup"><span data-stu-id="39b1d-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="39b1d-141">เมื่อคุณได้รับข้อความแจ้งให้องค์กรของคุณสามารถจัดการอุปกรณ์ได้ ให้เลือก **แอปนี้เท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="39b1d-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="39b1d-142">เมื่อการเรียกใช้งานเสร็จสมบูรณ์ ให้เลือก **เริ่มต้นใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="39b1d-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="39b1d-143">เปิดใช้งาน BOPIS ใน Modern POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="39b1d-144">ลงชื่อเข้าใช้ Modern POS โดยใช้ **000713** เป็นรหัสผู้ปฏิบัติงานและ **123** เป็นรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="39b1d-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="39b1d-145">ในขณะที่วิดีโอการฝึกปฏิบัติบทนำกำลังเล่นอยู่ ให้เลือกกล่องกาเครื่องหมายสองกล่องที่มุมล่างซ้ายของกล่องโต้ตอบ แล้วปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="39b1d-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="39b1d-146">ถ้าคุณไม่ได้รับพร้อมท์ให้ปิดกะ ให้เลื่อนไปที่ด้านขวาบนหน้า **ยินดีต้อนรับ** ให้เลือก **ปิดกะ** แล้วลงชื่อกลับเข้าสู่ POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="39b1d-147">หลังจากที่คุณลงชื่อเข้าใช้แล้ว เมื่อคุณได้รับข้อความแจ้ง ให้เลือก **ทำการดำเนินงานที่ไม่มีลิ้นชัก**</span><span class="sxs-lookup"><span data-stu-id="39b1d-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="39b1d-148">บนหน้า **ยินดีต้อนรับ** เลื่อนไปทางขวา และเลือกการดำเนินการ **เลือกสถานีฮาร์ดแวร์**</span><span class="sxs-lookup"><span data-stu-id="39b1d-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="39b1d-149">เลือก **จัดการ** ตั้งค่าตัวเลือก **ใช้สถานีฮาร์ดแวร์** เป็น **เปิด** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="39b1d-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="39b1d-150">ลงชื่อออกจาก POS และจากนั้น เข้าสู่ระบบกลับเข้าไปใหม่</span><span class="sxs-lookup"><span data-stu-id="39b1d-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="39b1d-151">หลังจากที่คุณลงชื่อเข้าใช้แล้ว ให้เลือก **เปิดกะใหม่** แล้วเลือก **ลิ้นชัก**</span><span class="sxs-lookup"><span data-stu-id="39b1d-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="39b1d-152">ดำเนินการสถานการณ์จำลอง BOPIS ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="39b1d-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="39b1d-153">สร้างใบสั่งหน้าร้านสำหรับการเบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="39b1d-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="39b1d-154">ไปที่ URL ที่คุณระบุไว้ในขั้นตอน [เริ่มต้นอีคอมเมิร์ซ](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) ในระหว่างการตั้งค่าคอนฟิกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="39b1d-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="39b1d-155">เลือกสินค้า และเลือก **เพิ่มไปยังรถเข็น**</span><span class="sxs-lookup"><span data-stu-id="39b1d-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="39b1d-156">บนหน้าถุงช้อปปิ้ง ให้เลือก **เบิกสินค้านี้** สำหรับรายการใบสั่งที่คุณเพิ่งเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="39b1d-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="39b1d-157">ในกล่องโต้ตอบ **เลือกร้านค้า** ให้ป้อน **San Francisco** แล้วเลือกปุ่ม **ค้นหา**</span><span class="sxs-lookup"><span data-stu-id="39b1d-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="39b1d-158">ในรายการของผลลัพธ์ ให้ค้นหาร้านค้า San Francisco และเลือก **เบิกสินค้าที่นี่**</span><span class="sxs-lookup"><span data-stu-id="39b1d-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="39b1d-159">บนหน้าถุงช้อปปิ้ง ให้เลือก **เช็คเอาท์ในฐานะผู้เยี่ยมชม**</span><span class="sxs-lookup"><span data-stu-id="39b1d-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="39b1d-160">เมื่อต้องการดำเนินการเช็คเอาท์ต่อไป คุณต้องยอมรับการแจ้งเตือนเกี่ยวกับคุกกี้</span><span class="sxs-lookup"><span data-stu-id="39b1d-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="39b1d-161">การแจ้งเตือนนี้จะปรากฏเป็นแบนเนอร์ที่ด้านบนของหน้าเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="39b1d-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="39b1d-162">สำหรับวิธีการชำระเงินด้วยบัตรเครดิต ให้ป้อนรายละเอียดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="39b1d-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="39b1d-163">**ชื่อผู้ถือบัตร:** ป้อนชื่อใดๆ</span><span class="sxs-lookup"><span data-stu-id="39b1d-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="39b1d-164">**หมายเลขบัตร:** ป้อน **4111-1111-1111-1111**</span><span class="sxs-lookup"><span data-stu-id="39b1d-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="39b1d-165">**วันหมดอายุ:** ป้อน **10/20**</span><span class="sxs-lookup"><span data-stu-id="39b1d-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="39b1d-166">**รหัสค่าการตรวจสอบความถูกต้องของบัตร (CVV):** ป้อน **737**</span><span class="sxs-lookup"><span data-stu-id="39b1d-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="39b1d-167">ห้ามลองใช้ข้อมูลบัตรเครดิตจริงในไซต์ทดสอบไม่ว่าในสถานการณ์ใดๆ ก็ตาม</span><span class="sxs-lookup"><span data-stu-id="39b1d-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="39b1d-168">ดำเนินการเช็คเอาท์ต่อโดยป้อนรายละเอียดของที่อยู่ในการเรียกเก็บเงิน แล้วเลือก **บันทึกและดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="39b1d-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="39b1d-169">เมื่อใบสั่งพร้อมใช้งานแล้ว ให้เลือก **เช็คเอาท์**</span><span class="sxs-lookup"><span data-stu-id="39b1d-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="39b1d-170">ซิงโครไนส์ใบสั่งออนไลน์ไปยังฝ่ายสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="39b1d-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="39b1d-171">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการซิงโครไนส์ใบสั่งออนไลน์ ให้ดูที่ [การลงรายการบัญชีการขายและการชำระเงินออนไลน์](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments)</span><span class="sxs-lookup"><span data-stu-id="39b1d-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="39b1d-172">เบิกสินค้าในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="39b1d-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="39b1d-173">ลงชื่อเข้าใช้ POS</span><span class="sxs-lookup"><span data-stu-id="39b1d-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="39b1d-174">บนหน้าจอ **ยินดีต้อนรับ** ให้เลือก **การเติมสินค้าตามใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="39b1d-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="39b1d-175">ในรายการของสินค้าสำหรับการเบิกสินค้า ให้เลือกรายการจากใบสั่งที่ถูกวางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="39b1d-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="39b1d-176">ในขณะที่เลือกรายการใบสั่งแล้ว ให้เลือก **เบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="39b1d-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="39b1d-177">มีการเพิ่มสินค้าในรายการลงในหน้าจอธุรกรรม และ **$0.00** แสดงเป็นยอดดุลที่ครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="39b1d-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="39b1d-178">เลือกยอดดุลที่ครบกำหนดชำระ **$0.00** หรือเลือกวิธีการชำระเงินใดๆ เพื่อสรุปธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="39b1d-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="39b1d-179">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="39b1d-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="39b1d-180">ใบสั่งออนไลน์ที่ดึงข้อมูลใน POS มียอดดุลที่ครบกำหนดที่ไม่ใช่ศูนย์</span><span class="sxs-lookup"><span data-stu-id="39b1d-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="39b1d-181">เมื่อมีการดึงข้อมูลใบสั่งสำหรับการเบิกสินค้าในร้านค้า ถ้ายอดดุลที่ครบกำหนดไม่ใช่ 0 (ศูนย์) โปรดตรวจสอบให้แน่ใจว่ามีการใช้ Modern POS และสถานีฮาร์ดแวร์ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="39b1d-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="39b1d-182">ถ้ามีการใช้ Cloud POS หรือ Modern POS สำหรับ iOS ให้ตรวจสอบให้แน่ใจว่ามีการใช้งานสถานีฮาร์ดแวร์ที่ใช้ร่วมกันอยู่</span><span class="sxs-lookup"><span data-stu-id="39b1d-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="39b1d-183">ต้องมีฟอร์มของสถานีฮาร์ดแวร์ที่ใช้งานอยู่บางฟอร์มเพื่อดึงข้อมูลการชำระเงินที่ทำผ่านระบบออนไลน์</span><span class="sxs-lookup"><span data-stu-id="39b1d-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="39b1d-184">ปัญหาทั่วไปเกี่ยวกับการบันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="39b1d-184">General issues with payment capture</span></span>

<span data-ttu-id="39b1d-185">สำหรับปัญหาทั่วไปทั้งหมด คุณควรปรึกษาล็อกเหตุการณ์ Modern POS หรือ Internet Information Services (IIS) Hardware Station เป็นขั้นตอนแรกเสมอ</span><span class="sxs-lookup"><span data-stu-id="39b1d-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="39b1d-186">คุณสามารถค้นหาล็อกเหล่านี้ภายใต้โหนดต่อไปนี้ในล็อกเหตุการณ์ของ Windows:</span><span class="sxs-lookup"><span data-stu-id="39b1d-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="39b1d-187">ล็อกแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="39b1d-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="39b1d-188">ล็อกแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="39b1d-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39b1d-189">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="39b1d-189">Additional resources</span></span>

[<span data-ttu-id="39b1d-190">ภาพรวมของสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="39b1d-191">เตรียมใช้งานสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="39b1d-192">ตั้งค่าคอนฟิกคุณลักษณะเสริมสำหรับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="39b1d-193">FAQ เกี่ยวกับสภาพแวดล้อมการประเมินของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="39b1d-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="39b1d-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="39b1d-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="39b1d-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="39b1d-196">พอร์ทัล Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="39b1d-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="39b1d-197">เว็บไซต์ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="39b1d-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="39b1d-198">ตัวเชื่อมต่อการชำระเงิน Adyen</span><span class="sxs-lookup"><span data-stu-id="39b1d-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="39b1d-199">การบันทึกเครื่องมือการชำระเงินออนไลน์ด้วยตัวเชื่อมต่อ Adyen</span><span class="sxs-lookup"><span data-stu-id="39b1d-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="39b1d-200">ภาพรวมของการชำระเงินผ่านช่องทาง Omni</span><span class="sxs-lookup"><span data-stu-id="39b1d-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
