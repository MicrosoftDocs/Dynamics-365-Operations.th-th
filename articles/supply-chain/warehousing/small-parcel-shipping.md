---
title: การจัดส่งพัสดุขนาดเล็ก
description: หัวข้อนี้แสดงข้อมูลทั่วไปเกี่ยวกับคุณลักษณะการจัดส่งพัสดุขนาดเล็ก คุณลักษณะนี้ช่วยให้ Microsoft Dynamics 365 Supply Chain Management สามารถส่งรายละเอียดเกี่ยวกับคอนเทนเนอร์ที่บรรจุให้บริษัทขนส่ง แล้วได้รับป้ายชื่อการจัดส่ง อัตราการจัดส่ง และหมายเลขการติดตามย้อนกลับจากบริษัทขนส่งนั้น
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910220"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="33fae-104">การจัดส่งพัสดุขนาดเล็ก</span><span class="sxs-lookup"><span data-stu-id="33fae-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33fae-105">คุณลักษณะการจัดส่งพัสดุขนาดเล็ก (SPS) ช่วยให้ Microsoft Dynamics 365 Supply Chain Management สามารถโต้ตอบกับบริษัทขนส่งโดยตรงโดยให้กรอบงานการสื่อสารผ่าน API ของบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="33fae-106">ฟังก์ชันนี้มีประโยชน์เมื่อคุณส่งใบสั่งขายแต่ละใบผ่านในเชิงพาณิชย์ แทนการใช้การจัดส่งคอนเทนเนอร์หรือการขนส่งน้อยกว่าที่มีการบรรทุก (LTL)</span><span class="sxs-lookup"><span data-stu-id="33fae-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="33fae-107">คุณลักษณะ SPS จะโต้ตอบกับบริษัทขนส่งของคุณผ่าน *กลไกจัดการอัตรา* เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="33fae-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="33fae-108">องค์กรของคุณต้องพัฒนากลไกจัดการอัตรานี้โดยร่วมมือกับบริการฮับบริษัทขนส่งหรือบริษัทขนส่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="33fae-109">กลไกจัดการอัตรานี้ช่วยให้ Supply Chain Management สามารถส่งรายละเอียดเกี่ยวกับคอนเทนเนอร์ที่บรรจุให้บริษัทขนส่งของคุณ แล้วได้รับป้ายชื่อการจัดส่ง อัตราการจัดส่ง และหมายเลขการติดตามย้อนกลับจากบริษัทขนส่งนั้น</span><span class="sxs-lookup"><span data-stu-id="33fae-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="33fae-110">อัตราค่าจัดส่งที่ส่งคืนจะถูกบวกเพิ่มเข้าไปในใบสั่งขายที่เกี่ยวข้องเป็นค่าธรรมเนียมเบ็ดเตล็ด</span><span class="sxs-lookup"><span data-stu-id="33fae-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="33fae-111">จากนั้นคุณสามารถพิมพ์ป้ายชื่อการจัดส่งที่ส่งคืนโดยอัตโนมัติได้โดยใช้เครื่องพิมพ์ Javabra Programming Language (ZPL) และใช้กับการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="33fae-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="33fae-112">บริษัทขนส่งจะสแกนป้ายชื่อการจัดส่งนี้เมื่อเบิกบรรจุภัณฑ์ที่คลังสินค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="33fae-113">การจัดเตรียมระบบของคุณเพื่อสนับสนุน SPS</span><span class="sxs-lookup"><span data-stu-id="33fae-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="33fae-114">ก่อนที่คุณจะสามารถเริ่มใช้ฟังก์ชัน SPS ได้ คุณต้องเปิดคุณลักษณะ SPS ในการจัดการคุณลักษณะ เพิ่มกลไกจัดการอัตราของคุณ และตั้งค่าโมดูล **การจัดการการขนส่ง** และ **การจัดการคลังสินค้า** เพื่อสนับสนุนคุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="33fae-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="33fae-115">เปิดคุณลักษณะ SPS</span><span class="sxs-lookup"><span data-stu-id="33fae-115">Turn on the SPS feature</span></span>

<span data-ttu-id="33fae-116">ก่อนที่คุณจะสามารถใช้คุณลักษณะ SPS คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="33fae-117">ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน หากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="33fae-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="33fae-118">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="33fae-119">**โมดูล:** *การจัดการการขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="33fae-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="33fae-120">**ชื่อคุณลักษณะ:** *การจัดส่งพัสดุขนาดเล็ก*</span><span class="sxs-lookup"><span data-stu-id="33fae-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="33fae-121">ปรับใช้และตั้งค่ากลไกจัดการอัตรา</span><span class="sxs-lookup"><span data-stu-id="33fae-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="33fae-122">Supply Chain Management ไม่มีกลไกจัดการอัตราใดๆ</span><span class="sxs-lookup"><span data-stu-id="33fae-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="33fae-123">คุณต้องได้รับหรือสร้างกลไกจัดการอัตราใด ๆ ที่คุณต้องการ แล้วเพิ่มกลไกจัดการอัตราเหล่านั้นลงในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="33fae-124">อย่างไรก็ตาม Microsoft มีกลไกจัดการอัตราสาธิตที่คุณสามารถใช้ในการทดสอบได้</span><span class="sxs-lookup"><span data-stu-id="33fae-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="33fae-125">ดาวน์โหลดและปรับใช้กลไกจัดการอัตราสาธิต</span><span class="sxs-lookup"><span data-stu-id="33fae-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="33fae-126">ให้ดำเนินการตามขั้นตอนต่อไปนี้เพื่อรับกลไกจัดการอัตราสาธิต</span><span class="sxs-lookup"><span data-stu-id="33fae-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="33fae-127">บน GitHub ให้ดาวน์โหลด [ไลบรารีแบบไดนามิกลิงค์ (DLL) ของกลไกจัดการอัตราสาธิต](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS)</span><span class="sxs-lookup"><span data-stu-id="33fae-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="33fae-128">บนเซิร์ฟเวอร์ Supply Chain Management ของคุณ ให้บันทึก DLL ในโฟลเดอร์ **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**</span><span class="sxs-lookup"><span data-stu-id="33fae-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="33fae-129">สร้างและปรับใช้กลไกจัดการอัตราฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="33fae-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="33fae-130">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและใช้งานกลไกจัดการอัตราฟังก์ชัน เพื่อให้สามารถใช้กลไกจัดการอัตราฟังก์ชันได้ในสภาพแวดล้อมการผลิตหรือการทดสอบ โปรดดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="33fae-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="33fae-131">สร้างกลไกจัดการการจัดการขนส่งใหม่</span><span class="sxs-lookup"><span data-stu-id="33fae-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="33fae-132">ตั้งค่ากลไกจัดการการจัดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="33fae-133">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างกลไกจัดการอัตรา SPS โปรดดูที่ประกาศบล็อกต่อไปนี้: [การจัดส่งพัสดุขนาดเล็ก: วิธีเพิ่มฟังก์ชันการจัดส่งพัสดุขนาดเล็กใน Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5)</span><span class="sxs-lookup"><span data-stu-id="33fae-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="33fae-134">การตั้งค่ากลไกจัดการอัตราใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="33fae-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="33fae-135">หลังจากที่คุณได้สร้างและปรับใช้กลไกจัดการอัตราของ SPS แล้ว ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="33fae-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="33fae-136">ไปที่ **การจัดการการขนส่ง \> \> กลไกจัดการ \> กลไกจัดการอัตรา**</span><span class="sxs-lookup"><span data-stu-id="33fae-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="33fae-137">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="33fae-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="33fae-138">บนแถวใหม่ ให้กำหนดฟิลด์ดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="33fae-139">**กลไกจัดการการจัดอันดับ** – ป้อนชื่อเฉพาะของกลไกจัดการอัตรา</span><span class="sxs-lookup"><span data-stu-id="33fae-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="33fae-140">ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *กลไกจัดการอัตราสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="33fae-141">**ชื่อ** – ป้อนคำอธิบายย่อเกี่ยวกับกลไกจัดการอัตรา</span><span class="sxs-lookup"><span data-stu-id="33fae-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="33fae-142">ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *กลไกจัดการอัตราสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="33fae-143">**รหัสข้อมูลเมตาของการจัดอันดับ** – เลือกข้อมูลพื้นฐานที่ควรใช้เพื่อคํานวณอัตราของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="33fae-144">ตัวอย่างเช่น อัตราของคุณอาจมีการคํานวณตามระยะทาง</span><span class="sxs-lookup"><span data-stu-id="33fae-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="33fae-145">ถ้าคุณกำลังใช้กลไกจัดการอัตราสาธิต คุณสามารถปล่อยฟิลด์นี้ให้ว่างไว้ได้</span><span class="sxs-lookup"><span data-stu-id="33fae-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="33fae-146">**แอสเซมบลีกลไกจัดการ** – ป้อนชื่อไฟล์ของแพคเกจ DLL ที่คุณจัดวาง</span><span class="sxs-lookup"><span data-stu-id="33fae-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="33fae-147">ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *TMSSmallParcelShippingEngine.dll*</span><span class="sxs-lookup"><span data-stu-id="33fae-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="33fae-148">**คลาสกลไกจัดการ** – ป้อนชื่อคลาสที่สร้างขึ้นสถาปนากลไกจัดการอัตราของคุณ</span><span class="sxs-lookup"><span data-stu-id="33fae-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="33fae-149">ถ้าคุณจะใช้กลไกจัดการอัตราสาธิต ให้ป้อน *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*</span><span class="sxs-lookup"><span data-stu-id="33fae-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="33fae-150">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="33fae-150">Example scenario</span></span>

<span data-ttu-id="33fae-151">สถานการณ์นี้แสดงวิธีการตั้งค่าและใช้ SPS หลังจากที่คุณได้จัดเตรียมระบบของคุณตามที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="33fae-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="33fae-152">สถานการณ์นี้จะใช้กลไกจัดการอัตราสาธิตที่ได้กล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="33fae-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="33fae-153">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="33fae-153">Make demo data available</span></span>

<span data-ttu-id="33fae-154">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าสาธิตที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="33fae-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="33fae-155">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="33fae-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="33fae-156">ตั้งค่าสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="33fae-156">Set up the scenario</span></span>

<span data-ttu-id="33fae-157">ตัวอย่างเช่น คุณต้องมีบริษัทขนส่งสาธิต กลุ่มบริษัทขนส่ง นโยบายการบรรจุ และโปรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="33fae-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="33fae-158">ส่วนย่อยต่อไปนี้อธิบายวิธีการจัดเตรียมเรกคอร์ดที่สถานการณ์นี้ต้องการ</span><span class="sxs-lookup"><span data-stu-id="33fae-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="33fae-159">ในสถานการณ์การผลิต โดยทั่วไป กระบวนการตั้งค่าจะคล้ายคลึงกับกระบวนการที่อธิบายไว้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="33fae-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="33fae-160">อย่างไรก็ตาม คุณจะตั้งค่าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="33fae-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="33fae-161">ตั้งค่าบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-161">Set up carriers</span></span>

<span data-ttu-id="33fae-162">ให้ดำเนินการตามขั้นตอนเหล่านี้เพื่อตั้งค่าบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="33fae-163">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="33fae-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="33fae-164">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="33fae-165">บนส่วนหัว ให้กำหนดค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="33fae-166">**บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="33fae-167">**ชื่อ:** *บริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="33fae-168">**โหมด:** *ภาคพื้นดิน*</span><span class="sxs-lookup"><span data-stu-id="33fae-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="33fae-169">บน FastTab **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="33fae-170">**การเรียกใช้งานบริษัทขนส่ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="33fae-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="33fae-171">**การเรียกใช้งานการจัดอันดับบริษัทขนส่ง:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="33fae-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="33fae-172">บนแท็บด่วน **บริการ** ให้เลือก **สร้าง** เพื่อเพิ่มบริการไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="33fae-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="33fae-173">ให้ตั้งค่าค่าต่อไปนี้สำหรับบริการใหม่:</span><span class="sxs-lookup"><span data-stu-id="33fae-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="33fae-174">**บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="33fae-175">**ชื่อ:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="33fae-176">**วิธีการขนส่ง:** *ภาคพื้นดิน*</span><span class="sxs-lookup"><span data-stu-id="33fae-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="33fae-177">ป้อนค่าตามต้องการสำหรับฟิลด์อื่น ๆ ทั้งหมดตามจำเป็น</span><span class="sxs-lookup"><span data-stu-id="33fae-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="33fae-178">(เมื่อคุณบันทึกเรกคอร์ดบริษัทขนส่งใหม่ วิธีการจัดส่งใหม่จะถูกสร้างขึ้น และฟิลด์ **วิธีการจัดส่ง** จะถูกตั้งค่าโดยอัตโนมัติ)</span><span class="sxs-lookup"><span data-stu-id="33fae-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="33fae-179">บนแท็บด่วน **โปรไฟล์การจัดอันดับ** เลือก **สร้าง** เพื่อเพิ่มโปรไฟล์การจัดอันดับไปยังตาราง</span><span class="sxs-lookup"><span data-stu-id="33fae-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="33fae-180">ให้ตั้งค่าค่าต่อไปนี้สำหรับโปรไฟล์ใหม่:</span><span class="sxs-lookup"><span data-stu-id="33fae-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="33fae-181">**โปรไฟล์การจัดอันดับ:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="33fae-182">**ชื่อ:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="33fae-183">**กลไกจัดการอัตรา:** *กลไกจัดการอัตราสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="33fae-184">ป้อนค่าตามต้องการสำหรับฟิลด์อื่น ๆ ทั้งหมดตามจำเป็น</span><span class="sxs-lookup"><span data-stu-id="33fae-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="33fae-185">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="33fae-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="33fae-186">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าบริษัทขนส่ง ให้ดูที่ [ตั้งค่าบริษัทขนส่ง](../transportation/tasks/set-up-shipping-carriers.md)</span><span class="sxs-lookup"><span data-stu-id="33fae-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="33fae-187">ตั้งค่าบัญชีบริการบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-187">Set up carrier service accounts</span></span>

<span data-ttu-id="33fae-188">ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าบัญชีบริการบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="33fae-189">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> การจัดอันดับ \> บัญชีบริการบริษัทขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="33fae-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="33fae-190">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มบัญชีบริการบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="33fae-191">ให้ตั้งค่าค่าต่อไปนี้สำหรับบัญชีใหม่:</span><span class="sxs-lookup"><span data-stu-id="33fae-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="33fae-192">**บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="33fae-193">**บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="33fae-194">**หมายเลขบัญชีลูกค้าของบริษัทขนส่ง:** หมายเลขบัญชีลูกค้าของบริษัทขนส่งที่ใช้ตรวจสอบความถูกต้องและพิสูจน์ตัวจริงของการเชื่อมต่อกับบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="33fae-195">บริษัทขนส่งของคุณจะระบุค่านี้</span><span class="sxs-lookup"><span data-stu-id="33fae-195">Your carrier will provide this value.</span></span> <span data-ttu-id="33fae-196">ถ้าคุณใช้บริการสาธิต คุณสามารถป้อนค่าหนึ่ง ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="33fae-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="33fae-197">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="33fae-197">**Site:** *6*</span></span>
    - <span data-ttu-id="33fae-198">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="33fae-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="33fae-199">บ่อยครั้งที่ค่า **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** เป็นค่าเดียวที่ต้องใช้ในการตรวจสอบความถูกต้องการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="33fae-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="33fae-200">อย่างไรก็ตาม ถ้าบริษัทขนส่งของคุณต้องการพารามิเตอร์การรับรองความถูกต้องเพิ่มเติม องค์กรของคุณควรเลือกเองหน้านี้เพื่อเพิ่มฟิลด์พิเศษตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="33fae-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="33fae-201">ตั้งค่านโยบายการบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="33fae-201">Set up a container packing policy</span></span>

<span data-ttu-id="33fae-202">ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่านโยบายการบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="33fae-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="33fae-203">ถ้าคุณยังไม่ได้ตั้งค่านิยามเครื่องพิมพ์ ZPL ให้ใช้แอปพลิเคชันตัวแทนการกำหนดเส้นทางเอกสารเพื่อตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="33fae-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="33fae-204">สำหรับข้อมูลเพิ่มเติม ให้ดู [ภาพรวมการพิมพ์เอกสาร](../../fin-ops-core/dev-itpro/analytics/print-documents.md) และหัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="33fae-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="33fae-205">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> นโยบายการบรรจุคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="33fae-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="33fae-206">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มนโยบายการบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="33fae-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="33fae-207">ในส่วนหัวของนโยบายใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="33fae-208">**นโยบายการบรรจุคอนเทนเนอร์:** *นโยบายการบรรจุสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="33fae-209">**คำอธิบาย:** ป้อนคำอธิบายเกี่ยวกับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="33fae-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="33fae-210">บน FastTab **ภาพรวม** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="33fae-211">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="33fae-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="33fae-212">**สถานที่เริ่มต้นในการจัดส่งขั้นสุดท้าย:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="33fae-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="33fae-213">**น้ำหนักต่อหน่วย:** *กก.*</span><span class="sxs-lookup"><span data-stu-id="33fae-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="33fae-214">**นโยบายการปิดคอนเทนเนอร์:** *การนำออกใช้โดยอัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="33fae-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="33fae-215">**นโยบายการปล่อยคอนเทนเนอร์:** *พร้อมใช้งานที่สถานที่จัดส่งสุดท้าย*</span><span class="sxs-lookup"><span data-stu-id="33fae-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="33fae-216">บนแท็บด่วน **รายการคอนเทนเนอร์** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="33fae-217">**รายการอัตโนมัติเมื่อปิดคอนเทนเนอร์:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="33fae-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="33fae-218">**ข้อกำหนดรายการของคอนเทนเนอร์:** *การจัดการการขนส่ง*</span><span class="sxs-lookup"><span data-stu-id="33fae-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="33fae-219">**พิมพ์เนื้อหาของคอนเทนเนอร์:** *ไม่ใช่*</span><span class="sxs-lookup"><span data-stu-id="33fae-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="33fae-220">บนแท็บด่วน **การพิมพ์ป้ายชื่อบริษัทขนส่ง** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="33fae-221">**พิมพ์ป้ายชื่อการจัดส่งคอนเทนเนอร์:** *เสมอ*</span><span class="sxs-lookup"><span data-stu-id="33fae-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="33fae-222">**ชื่อเครื่องพิมพ์:** ชื่อของเครื่องพิมพ์ ZPL ที่ควรพิมพ์ป้ายชื่อการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="33fae-223">ตั้งค่าโพรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="33fae-223">Set up a packing profile</span></span>

<span data-ttu-id="33fae-224">ให้ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าโปรไฟล์การบรรจุ</span><span class="sxs-lookup"><span data-stu-id="33fae-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="33fae-225">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การบรรจุ \> โปรไฟล์การบรรจุ**</span><span class="sxs-lookup"><span data-stu-id="33fae-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="33fae-226">ในบานหน้าต่างการดำเนินการ ให้เลือก **ใหม่** เพื่อเพิ่มโปรไฟล์การบรรจุไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="33fae-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="33fae-227">ให้ตั้งค่าค่าต่อไปนี้สำหรับโปรไฟล์ใหม่:</span><span class="sxs-lookup"><span data-stu-id="33fae-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="33fae-228">**รหัสโปรไฟล์การบรรจุ:** *โปรไฟล์การบรรจุสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="33fae-229">**คำอธิบาย:** ป้อนคำอธิบายเกี่ยวกับโปรไฟล์</span><span class="sxs-lookup"><span data-stu-id="33fae-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="33fae-230">**นโยบายการบรรจุคอนเทนเนอร์:** *นโยบายการบรรจุสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="33fae-231">**โหมดรหัสคอนเทนเนอร์:** *อัตโนมัติ*</span><span class="sxs-lookup"><span data-stu-id="33fae-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="33fae-232">**ชนิดคอนเทนเนอร์:** *กล่องขนาดเล็ก*</span><span class="sxs-lookup"><span data-stu-id="33fae-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="33fae-233">การตั้งค่าลูกค้าเพื่อใช้บริษัทขนส่ง SPS</span><span class="sxs-lookup"><span data-stu-id="33fae-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="33fae-234">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าลูกค้าเพื่อให้สามารถใช้บริษัทขนส่งที่คุณสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="33fae-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="33fae-235">ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="33fae-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="33fae-236">ในตารางนี้ ให้ค้นหาและเลือกลูกค้า *US-027*</span><span class="sxs-lookup"><span data-stu-id="33fae-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="33fae-237">บนบานหน้าต่างการดำเนินการ บนแท็บ **ทั่วไป** ในกลุ่ม **การตั้งค่า** ให้เลือก **บัญชีลูกค้าของบริษัทขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="33fae-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="33fae-238">บนหน้า **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มบัญชีลงในกริด</span><span class="sxs-lookup"><span data-stu-id="33fae-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="33fae-239">ให้ตั้งค่าค่าต่อไปนี้สำหรับบัญชีใหม่:</span><span class="sxs-lookup"><span data-stu-id="33fae-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="33fae-240">**บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="33fae-241">**หมายเลขบัญชีลูกค้าของบริษัทขนส่ง:** *12345* (ค่าไม่สําคัญต่อสถานการณ์นี้ แต่ค่าจะอ้างอิงถึงในส่วนถัดไป)</span><span class="sxs-lookup"><span data-stu-id="33fae-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="33fae-242">ผ่านสถานการณ์ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="33fae-242">Go through the example scenario</span></span>

<span data-ttu-id="33fae-243">หลังจากที่คุณตั้งค่าข้อมูลตัวอย่างทั้งหมดตามที่อธิบายไว้ในส่วนก่อนหน้านี้แล้ว คุณพร้อมแล้วที่จะผ่านสถานการณ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="33fae-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="33fae-244">สร้างผลใบสั่งขายและประมวลผลงาน</span><span class="sxs-lookup"><span data-stu-id="33fae-244">Create a sales order and process the work</span></span>

<span data-ttu-id="33fae-245">ให้ปฏิบัติตามขั้นตอนเหล่านี้ในการสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="33fae-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="33fae-246">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="33fae-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="33fae-247">เลือก **สร้าง** เพื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="33fae-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="33fae-248">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-027*</span><span class="sxs-lookup"><span data-stu-id="33fae-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="33fae-249">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="33fae-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="33fae-250">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="33fae-250">The new sales order is opened.</span></span> <span data-ttu-id="33fae-251">บนแท็บด่วน **ส่วนหน้าของใบสั่งขาย** ให้ตั้งค่าฟิลด์ **หมายเลขบัญชีลูกค้าของบริษัทขนส่ง** เป็นค่าที่คุณเลือกไว้ของลูกค้ารายนี้ก่อนหน้านี้ (*12345*)</span><span class="sxs-lookup"><span data-stu-id="33fae-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="33fae-252">ในส่วน **บรรทัดใบสั่งขาย** ให้เพิ่มรายการขาย และตั้งค่าต่อไปนี้ให้กับบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="33fae-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="33fae-253">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="33fae-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="33fae-254">**ปริมาณ:** *1*</span><span class="sxs-lookup"><span data-stu-id="33fae-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="33fae-255">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="33fae-255">**Site:** *6*</span></span>
    - <span data-ttu-id="33fae-256">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="33fae-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="33fae-257">สลับไปยังมุมมอง **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="33fae-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="33fae-258">บนแท็บด่วน **การจัดส่ง** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="33fae-259">**บริษัทขนส่ง:** *บริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="33fae-260">**บริการบริษัทขนส่ง:** *บริการบริษัทขนส่งสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="33fae-261">สลับกลับไปยังมุมมอง **รายการ**</span><span class="sxs-lookup"><span data-stu-id="33fae-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="33fae-262">หากคุณได้รับพร้อมต์ให้อัพเดตวิธีการจัดส่งรายการขาย ให้เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="33fae-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="33fae-263">ในส่วน **บรรทัดใบสั่งขาย** ให้เลือกบรรทัดใบสั่งที่คุณตั้งค่าไว้ก่อนหน้านี้ แล้วเลือก **สินค้าคงคลัง \> การจอง**</span><span class="sxs-lookup"><span data-stu-id="33fae-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="33fae-264">บนหน้า **การจอง** ให้เลือก **สำรองล็อต** เพื่อจองปริมาณทั้งหมดของรายการที่เลือกในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="33fae-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="33fae-265">ปิดหน้า **การจอง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="33fae-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="33fae-266">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="33fae-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="33fae-267">งานถูกสร้างเพื่อย้ายสินค้าจากสถานที่เบิกสินค้าไปยังสถานีบรรจุ</span><span class="sxs-lookup"><span data-stu-id="33fae-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="33fae-268">ในส่วน **รายการในใบสั่งขาย** ให้เลือก **คลังสินค้า \> รายละเอียดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="33fae-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="33fae-269">บนหน้า **รายละเอียดการจัดส่ง** ให้บันทึกรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="33fae-270">คุณจะต้องใช้บรรจุภัณฑ์เมื่อคุณบรรจุสินค้าที่สถานีบรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="33fae-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="33fae-271">ปิดหน้า **รายละเอียดการจัดส่ง** เพื่อส่งคืนไปยังใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="33fae-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="33fae-272">จดบันทึกหมายเลขใบสั่งขาย แล้วไปที่ **การจัดการคลังสินค้า \> งาน \> งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="33fae-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="33fae-273">ใช้หมายเลขใบสั่งขายเพื่อค้นหาและเลือกงานที่สร้างขึ้นแล้วของใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="33fae-274">บนบานหน้าต่างการดำเนินการ บนแท็บ **งาน** เลือก **ทำงานให้เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="33fae-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="33fae-275">ในหน้า **การเสร็จสมบูรณ์ของงาน** ในฟิลด์ **รหัสผู้ใช้** ให้เลือกรหัสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="33fae-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="33fae-276">จากนั้น ในบานหน้าต่างการดำเนินการ เลือก **ตรวจสอบความถูกต้องของงาน**</span><span class="sxs-lookup"><span data-stu-id="33fae-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="33fae-277">หากงานผ่านการตรวจสอบความถูกต้อง ให้เลือก **ทำงานให้เสร็จสมบูรณ์** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="33fae-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="33fae-278">งานถูกกําหนดเป็นเสร็จสมบูรณ์แล้วเพื่อจําลองการย้ายสินค้าไปยังสถานีบรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="33fae-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="33fae-279">การบรรจุการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-279">Pack the shipment</span></span>

<span data-ttu-id="33fae-280">ให้ทำตามขั้นตอนเหล่านี้เพื่อบรรจุการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="33fae-281">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> ผู้ปฏิบัติงาน** และตรวจสอบให้แน่ใจว่าบัญชีผู้ใช้ของคุณเชื่อมโยงกับบัญชีผู้ปฏิบัติงานในการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="33fae-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="33fae-282">ไปที่ **การจัดการคลังสินค้า \> การเบิกสินค้าและการบรรจุลงตู้บรรจุสินค้า \> บรรจุ**</span><span class="sxs-lookup"><span data-stu-id="33fae-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="33fae-283">ในกล่องโต้ตอบ **เลือกสถานีบรรจุ** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="33fae-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="33fae-284">**ไซต์:** *6*</span><span class="sxs-lookup"><span data-stu-id="33fae-284">**Site:** *6*</span></span>
    - <span data-ttu-id="33fae-285">**คลังสินค้า:** *62*</span><span class="sxs-lookup"><span data-stu-id="33fae-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="33fae-286">**สถานที่:** *บรรจุ*</span><span class="sxs-lookup"><span data-stu-id="33fae-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="33fae-287">**รหัสโปรไฟล์การบรรจุ:** *โปรไฟล์การบรรจุสาธิต*</span><span class="sxs-lookup"><span data-stu-id="33fae-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="33fae-288">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="33fae-288">Select **OK**.</span></span>
1. <span data-ttu-id="33fae-289">หน้า **บรรจุ** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="33fae-289">The **Pack** page appears.</span></span> <span data-ttu-id="33fae-290">ในสถานการณ์สถานการณ์การผลิต ผู้ปฏิบัติงานจะสแกนป้ายทะเบียนหรือรหัสการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="33fae-291">อย่างไรก็ตาม ในสถานการณ์นี้ ให้เปิดหน้า **การจัดส่งสินค้าทั้งหมด** และค้นหาหมายเลขการจัดส่งของการจัดส่งที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="33fae-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="33fae-292">แล้วป้อนค่านี้ในฟิลด์ **ป้ายทะเบียนหรือการจัดส่ง** บนหน้า **บรรจุ**</span><span class="sxs-lookup"><span data-stu-id="33fae-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="33fae-293">หรือป้อนรหัสการจัดส่งที่คุณจดบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="33fae-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="33fae-294">บนหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="33fae-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="33fae-295">กล่องโต้ตอบที่ปรากฏจะแสดงรายละเอียดเกี่ยวกับคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="33fae-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="33fae-296">ปล่อยค่าเริ่มต้น แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="33fae-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="33fae-297">บนหน้า **บรรจุ** บนแท็บด่วน **การบรรจุสินค้า** ในฟิลด์ **ตัวระบุ** ให้เลือก *A0002* เพื่อบรรจุสินค้านั้น</span><span class="sxs-lookup"><span data-stu-id="33fae-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="33fae-298">สินค้าจะถูกเพิ่มลงในคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="33fae-298">The item is added to the container.</span></span>
1. <span data-ttu-id="33fae-299">บนบานหน้าต่างการดำเนินการ เลือก **คอนเทนเนอร์สำหรับการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="33fae-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="33fae-300">บนหน้า **คอนเทนเนอร์สำหรับการจัดส่ง** ที่ปรากฏจะมีแถวของคอนเทนเนอร์ที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="33fae-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="33fae-301">อย่างไรก็ตาม ฟิลด์ **รหัสรายการคอนเทนเนอร์** ในแถวนั้นว่างเปล่าในปัจจุบัน เนื่องจากคุณยังไม่ได้รับป้ายชื่อการจัดส่งและหมายเลขการติดตามจากบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="33fae-302">บนหน้าต่างการดำเนินการ เลือก **ปิดคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="33fae-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="33fae-303">ในกล่องโต้ตอบ **ปิดคอนเทนเนอร์** ให้ตั้งค่าฟิลด์ **น้ำหนักรวม** เป็น *1 กก.* แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="33fae-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="33fae-304">ตอนนี้ ควรพิมพ์ป้ายชื่อการจัดส่งบนเครื่องพิมพ์ ZPL ที่คุณเลือกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="33fae-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="33fae-305">ผลลัพธ์ควรมีลักษณะคล้ายกับตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="33fae-305">It should resemble the following example.</span></span>

    <span data-ttu-id="33fae-306">![ตัวอย่างป้ายชื่อการจัดส่ง](media/sps-label-example.png "ตัวอย่างป้ายชื่อการจัดส่ง")</span><span class="sxs-lookup"><span data-stu-id="33fae-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="33fae-307">โปรดสังเกตว่า ค่า **รหัสรายการคอนเทนเนอร์** และ **การขนส่งรวม** ถูกเพิ่มเมื่อได้รับจากบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="33fae-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]