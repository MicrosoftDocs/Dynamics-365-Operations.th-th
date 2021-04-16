---
title: ตั้งค่ามิติที่แตกต่างกันเกี่ยวกับการบรรจุและการจัดเก็บ
description: หัวข้อนี้แสดงวิธีการระบุกระบวนการที่ (การบรรจุ การจัดเก็บ หรือการบรรจุที่ซ้อนกัน) แต่ละมิติที่ระบุจะใช้
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818931"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="2b7f0-103">ตั้งค่ามิติที่แตกต่างกันเกี่ยวกับการบรรจุและการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b7f0-104">สินค้าบางรายการจะถูกบรรจุหรือจัดเก็บในลักษณะที่คุณอาจต้องใช้ในการติดตามมิติทางกายภาพที่แตกต่างกันในแต่ละกระบวนการที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="2b7f0-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="2b7f0-105">คุณลักษณะ *มิติของผลิตภัณฑ์บรรจุภัณฑ์* ช่วยให้คุณตั้งค่ามิติหนึ่งชนิดขึ้นไปให้กับผลิตภัณฑ์แต่ละรายการได้</span><span class="sxs-lookup"><span data-stu-id="2b7f0-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="2b7f0-106">แต่ละชนิดมิติจะมีชุดของการวัดทางกายภาพ (น้ำหนัก ความกว้าง ความลึก และความสูง) และกําหนดกระบวนการที่ใช้ค่าการวัดทางกายภาพดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="2b7f0-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="2b7f0-107">เมื่อเปิดใช้งานคุณลักษณะนี้ ระบบของคุณจะสนับสนุนชนิดของมิติต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="2b7f0-108">*การจัดเก็บ* - มิติการจัดเก็บจะใช้พร้อมกับเชิงปริมาตรของสถานที่เก็บ เพื่อระบุว่าสามารถจัดเก็บสินค้าแต่ละรายการในสถานที่ตั้งคลังสินค้าต่าง ๆ ได้จำนวนเท่าใด</span><span class="sxs-lookup"><span data-stu-id="2b7f0-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="2b7f0-109">*การบรรจุ* - มิติการบรรจุจะใช้ระหว่างการบรรจุลงตู้บรรจุสินค้าและกระบวนการบรรจุเองเพื่อกำหนดว่าปริมาณสินค้าเท่าใดของแต่ละรายการจะพอดีกับชนิดคอนเทนเนอร์ต่างๆ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="2b7f0-110">*การบรรจุที่ซ้อนกัน* - มิติการบรรจุที่ซ้อนกันจะใช้เมื่อกระบวนการบรรจุประกอบด้วยหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="2b7f0-111">มิติ *การจัดเก็บ* ได้รับการสนับสนุนแม้ว่าคุณลักษณะ *มิติของผลิตภัณฑ์บรรจุภัณฑ์* จะไม่เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="2b7f0-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="2b7f0-112">คุณตั้งค่าเหล่านี้โดยใช้หน้า **มิติทางกายภาพ** ใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2b7f0-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="2b7f0-113">มิติเหล่านี้สามารถใช้ได้โดยกระบวนการทั้งหมดที่ไม่ได้ระบุมิติการบรรจุและมิติการบรรจุที่ซ้อนกัน</span><span class="sxs-lookup"><span data-stu-id="2b7f0-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="2b7f0-114">มิติ *การบรรจุ* และ *การบรรจุที่ซ้อนกัน* มีการตั้งค่าโดยใช้หน้า **มิติของผลิตภัณฑ์ทางกายภาพ** ซึ่งเพิ่มเมื่อคุณเปิดใช้งานคุณลักษณะ *มิติของผลิตภัณฑ์บรรจุภัณฑ์*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="2b7f0-115">หัวข้อนี้มีสถานการณ์ที่แสดงให้เห็นวิธีการใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="2b7f0-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="2b7f0-116">เปิดคุณลักษณะมิติของผลิตภัณฑ์บรรจุภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b7f0-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="2b7f0-117">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2b7f0-118">ผู้ดูแลระบบสามารถใช้พื้นที่การทำงาน [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานหากจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2b7f0-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2b7f0-119">มีคุณลักษณะที่แสดงอยู่ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2b7f0-120">**โมดูล:** *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2b7f0-121">**ชื่อคุณลักษณะ:** *มิติของผลิตภัณฑ์บรรจุภัณฑ์*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2b7f0-122">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="2b7f0-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="2b7f0-123">ตั้งค่าสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="2b7f0-123">Set up the scenario</span></span>

<span data-ttu-id="2b7f0-124">ก่อนที่คุณจะสามารถรันสถานการณ์ตัวอย่างได้ คุณต้องจัดเตรียมระบบของคุณตามที่อธิบายไว้ในส่วนนี้</span><span class="sxs-lookup"><span data-stu-id="2b7f0-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="2b7f0-125">เปิดใช้งานข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="2b7f0-125">Enable demo data</span></span>

<span data-ttu-id="2b7f0-126">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าสาธิตที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="2b7f0-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="2b7f0-127">นอกจากนี้ คุณยังต้องเลือกนิติบุคคล *USMF* ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="2b7f0-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="2b7f0-128">เพิ่มมิติทางกายภาพใหม่ให้กับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="2b7f0-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="2b7f0-129">เพิ่มมิติทางกายภาพใหม่ให้กับผลิตภัณฑ์โดยทำตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="2b7f0-130">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="2b7f0-131">เลือกผลิตภัณฑ์ที่มี **หมายเลขสินค้า** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="2b7f0-132">บนบานหน้าต่างการดำเนินการ เปิดแท็บ **จัดการสินค้าคงคลัง** และจากกลุ่ม **คลังสินค้า** เลือก **มิติของผลิตภัณฑ์ทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="2b7f0-133">หน้า **มิติของผลิตภัณฑ์ทางกายภาพ** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="2b7f0-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="2b7f0-134">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อเพิ่มมิติใหม่ไปยังกริดด้วยการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="2b7f0-135">**ชนิดมิติทางกายภาพ** - *การบรรจุ*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="2b7f0-136">**หน่วยทางกายภาพ** - *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="2b7f0-137">**น้ำหนัก** - *4*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="2b7f0-138">**น้ำหนักต่อหน่วย** - *กก.*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="2b7f0-139">**ความลึก** - *3*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="2b7f0-140">**ความสูง** - *4*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-140">**Height** - *4*</span></span>
    - <span data-ttu-id="2b7f0-141">**ความกว้าง** - *3*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-141">**Width** - *3*</span></span>
    - <span data-ttu-id="2b7f0-142">**ความยาว** - *ซม.*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="2b7f0-143">**หน่วยปริมาตร** - *ซม.3*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="2b7f0-144">ฟิลด์ **ปริมาตร** จะถูกคํานวณโดยอัตโนมัติตามการตั้งค่า **ความลึก** **ความสูง** และ **ความกว้าง** ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="2b7f0-145">สร้างชนิดคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="2b7f0-145">Create a new container type</span></span>

<span data-ttu-id="2b7f0-146">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> ชนิดคอนเทนเนอร์** และสร้างเรกคอร์ดใหม่ด้วยการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b7f0-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="2b7f0-147">**รหัสชนิดคอนเทนเนอร์** - *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="2b7f0-148">**คำอธิบาย** - *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="2b7f0-149">**น้ำหนักสุทธิสูงสุด** - *50*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="2b7f0-150">**ปริมาตร** - *144*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-150">**Volume** - *144*</span></span>
- <span data-ttu-id="2b7f0-151">**ความยาว** - *6*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-151">**Length** - *6*</span></span>
- <span data-ttu-id="2b7f0-152">**ความกว้าง** - *6*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-152">**Width** - *6*</span></span>
- <span data-ttu-id="2b7f0-153">**ความสูง** - *4*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="2b7f0-154">สร้างกลุ่มคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="2b7f0-154">Create a container group</span></span>

<span data-ttu-id="2b7f0-155">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> กลุ่มคอนเทนเนอร์** และสร้างเรกคอร์ดใหม่ด้วยการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2b7f0-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="2b7f0-156">**รหัสกลุ่มคอนเทนเนอร์** - *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="2b7f0-157">**คำอธิบาย** - *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="2b7f0-158">เพิ่มบรรทัดใหม่ลงในส่วน **รายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="2b7f0-159">ตั้งค่า **ชนิดคอนเทนเนอร์** เป็น *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="2b7f0-160">ตั้งค่าเท็มเพลตการสร้างตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="2b7f0-160">Set up a container build template</span></span>

<span data-ttu-id="2b7f0-161">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> คอนเทนเนอร์ \> แม่แบบการสร้างคอนเทนเนอร์** และเลือก **กล่อง**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="2b7f0-162">เปลี่ยน **รหัสกลุ่มคอนเทนเนอร์** เป็น *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="2b7f0-163">เรียกใช้สถานการณ์</span><span class="sxs-lookup"><span data-stu-id="2b7f0-163">Run the scenario</span></span>

<span data-ttu-id="2b7f0-164">หลังจากที่คุณได้จัดเตรียมระบบของคุณตามที่อธิบายไว้ในส่วนก่อนหน้านี้แล้ว คุณพร้อมที่จะเรียกใช้สถานการณ์ที่อธิบายไว้ในส่วนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2b7f0-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="2b7f0-165">สร้างใบสั่งขายและสร้างการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="2b7f0-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="2b7f0-166">ในกระบวนการนี้ คุณจะสร้างการจัดส่งสินค้าตามมิติ *การบรรจุ* ซึ่งมีความสูงน้อยกว่า 3</span><span class="sxs-lookup"><span data-stu-id="2b7f0-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="2b7f0-167">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="2b7f0-168">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2b7f0-169">ในกล่องโต้ตอบ **สร้างใบสั่งขาย** ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2b7f0-170">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="2b7f0-171">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="2b7f0-172">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="2b7f0-173">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="2b7f0-173">The new sales order is opened.</span></span> <span data-ttu-id="2b7f0-174">ฟิลด์นี้ควรมีบรรทัดใหม่ว่างเปล่าในกริดบนแท็บด่วน **บรรทัดใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="2b7f0-175">บนบรรทัดนี้ ให้ตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="2b7f0-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="2b7f0-176">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="2b7f0-177">**ปริมาณ:** *5*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="2b7f0-178">บนแท็บด่วน **รายการใบสั่งขาย** เลือก **สินค้าคงคลัง \> การจองสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="2b7f0-179">ในหน้า **การจอง** บนบานหน้าต่างการดำเนินการ เลือก **จองล็อต** เพื่อจองสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="2b7f0-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="2b7f0-180">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2b7f0-180">Close the page.</span></span>
1. <span data-ttu-id="2b7f0-181">บนบานหน้าต่างการดำเนินการ เปิดแท็บ **คลังสินค้า** และเลือก **นำออกใช้ไปยังคลังสินค้า** เพื่อสร้างงานสำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="2b7f0-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="2b7f0-182">บนแท็บด่วน **รายการในใบสั่งขาย** ให้เลือก **คลังสินค้า \> รายละเอียดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="2b7f0-183">ในบานหน้าต่างการดำเนินการ ให้เปิดแท็บ **การขนส่ง** แล้วเลือก **ดูคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="2b7f0-184">ยืนยันว่าสินค้าถูกบรรจุลงในตู้บรรจุสินค้าแบบ *กล่องสั้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="2b7f0-185">วางสินค้าลงในการจัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="2b7f0-185">Place an item into storage</span></span>

1. <span data-ttu-id="2b7f0-186">เปิดอุปกรณ์เคลื่อนที่ เข้าสู่ระบบคลังสินค้า 63 และไปที่ **สินค้าคงคลัง \> ปรับปรุงใน**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="2b7f0-187">ป้อน **Loc** = *SHORT-01*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="2b7f0-188">สร้างป้ายทะเบียนใหม่ด้วย **สินค้า** = *A0001* และ **ปริมาณ** = *1 ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="2b7f0-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="2b7f0-189">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2b7f0-189">Select **OK**.</span></span> <span data-ttu-id="2b7f0-190">คุณจะได้รับข้อผิดพลาด "ที่ตั้ง SHORT-01ล้มเหลว เนื่องจากสินค้า A0001 ไม่พอดีกับมิติที่ระบุของสถานที่"</span><span class="sxs-lookup"><span data-stu-id="2b7f0-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="2b7f0-191">เนื่องจากมิติชนิด *การจัดเก็บ* ของผลิตภัณฑ์มีขนาดใหญ่กว่ามิติที่ระบุในโปรไฟล์สถานที่</span><span class="sxs-lookup"><span data-stu-id="2b7f0-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]