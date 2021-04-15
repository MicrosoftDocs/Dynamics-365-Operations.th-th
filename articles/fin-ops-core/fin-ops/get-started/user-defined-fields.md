---
title: สร้างและทำงานกับฟิลด์ที่กำหนดเอง
description: หัวข้อนี้แสดงวิธีการสร้างฟิลด์แบบกำหนดเองผ่านอินเทอร์เฟซผู้ใช้เพื่อปรับแต่งแอพลิเคชันให้เหมาะกับธุรกิจของคุณ
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: a07c1a81f0436664acdfd23975a99c6670c6fb1c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754763"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="afd14-103">สร้างและทำงานกับฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afd14-104">ในขณะที่มีชุดที่ขยายขอบเขตของฟิลด์แบบนอกกรอบสำหรับการจัดการกระบวนการทางธุรกิจที่หลากหลาย ในบางครั้งมีความต้องการสำหรับบริษัทในการติดตามข้อมูลเพิ่มเติมในระบบ</span><span class="sxs-lookup"><span data-stu-id="afd14-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="afd14-105">ในขณะที่สามารถใช้โปรแกรมเมอร์เพื่อเพิ่มฟิลด์เหล่านั้นเป็นส่วนขยายในเครื่องมือสำหรับนักพัฒนาได้ คุณลักษณะของฟิลด์ที่กำหนดเองจะช่วยให้คุณสามารถเพิ่มฟิลด์ได้โดยตรงจากอินเทอร์เฟซผู้ใช้ ซึ่งช่วยให้คุณสามารถปรับแต่งแอพลิเคชันเพื่อให้เหมาะสมกับธุรกิจของคุณโดยใช้เว็บเบราเซอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="afd14-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="afd14-106">ความสามารถในการเพิ่มฟิลด์ที่กำหนดเองจะพร้อมใช้งานในการปรับปรุงแพลตฟอร์ม 13 และรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="afd14-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="afd14-107">เฉพาะผู้ใช้ที่มีสิทธิ์พิเศษเท่านั้นที่สามารถเข้าถึงคุณลักษณะนี้ได้</span><span class="sxs-lookup"><span data-stu-id="afd14-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="afd14-108">วิดีโอนี้แสดงความง่ายดายในการเพิ่มฟิลด์ที่กำหนดเองลงในหน้า: [การเพิ่มฟิลด์ที่กำหนดเองใน](https://www.youtube.com/watch?v=gWSGZI9Vtnc)</span><span class="sxs-lookup"><span data-stu-id="afd14-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="afd14-109">การสร้างฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-109">Creating custom fields</span></span>

<span data-ttu-id="afd14-110">หลังจากที่คุณได้ระบุข้อมูลเพิ่มเติมที่คุณต้องการติดตามในใบสมัคร คุณสามารถสร้างฟิลด์แบบกำหนดเองในตารางที่เหมาะสม และแสดงถึงฟิลด์ใหม่ในหน้าได้</span><span class="sxs-lookup"><span data-stu-id="afd14-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="afd14-111">ขั้นตอนต่อไปนี้อธิบายกระบวนการสำหรับการสร้างฟิลด์แบบกำหนดเอง และการใส่ฟิลด์นั้นในแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="afd14-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="afd14-112">นำทางไปยังแบบฟอร์มที่ซึ่งจำเป็นต้องมีฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="afd14-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="afd14-113">เนื่องจากเป้าหมายสุดท้ายคือ การแสดงถึงฟิลด์ที่กำหนดเองในแบบฟอร์ม จุดป้อนข้อมูลสำหรับการสร้างฟิลด์ที่กำหนดเองมีอยู่ภายในประสบการณ์ใช้งานการตั้งค่าส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="afd14-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="afd14-114">เปิดแถบเครื่องมือการตั้งค่าส่วนบุคคล โดยการเลือก **ตัวเลือก** และจากนั้น **กำหนดแบบฟอร์มนี้ให้เป็นแบบส่วนบุคคล**</span><span class="sxs-lookup"><span data-stu-id="afd14-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="afd14-115">คลิก **แทรก** และจากนั้น **ฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="afd14-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="afd14-116">เลือกภูมิภาคของแบบฟอร์มที่คุณต้องการแสดงฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="afd14-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="afd14-117">หลังจากการเลือก กล่องโต้ตอบ **แทรกฟิลด์** จะแสดงรายการของฟิลด์ที่มีอยู่ที่สามารถแทรกลงในพื้นที่ที่เลือกของแบบฟอร์มได้</span><span class="sxs-lookup"><span data-stu-id="afd14-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="afd14-118">ให้แน่ใจว่า ฟิลด์ที่คุณสนใจยังไม่มีอยู่ในรายการ</span><span class="sxs-lookup"><span data-stu-id="afd14-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="afd14-119">ถ้าเป็นเช่นนั้น คุณสามารถเลือกฟิลด์นั้นในรายการได้อย่างง่ายดาย และคลิก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="afd14-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="afd14-120">คลิกปุ่ม **สร้างฟิลด์ใหม่** ด้านบนรายการเพื่อเริ่มต้นกระบวนการสร้างฟิลด์แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="afd14-121">นี่จะเปิดกล่องโต้ตอบ **สร้างฟิลด์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="afd14-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="afd14-122">ถ้าคุณไม่เห็นปุ่ม **สร้างฟิลด์ใหม่** คุณไม่มีสิทธิ์ที่จำเป็นในการใช้คุณลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="afd14-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="afd14-123">ในกล่องโต้ตอบ **สร้างฟิลด์ใหม่** ให้ป้อนข้อมูลดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="afd14-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="afd14-124">เลือกตารางฐานข้อมูลที่ซึ่งฟิลด์นี้ควรถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="afd14-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="afd14-125">โปรดทราบว่า เฉพาะตารางที่สนับสนุนฟิลด์แบบกำหนดเองจะปรากฏขึ้นในรายการแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="afd14-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="afd14-126">ดูส่วนด้านล่างสำหรับรายละเอียดทางเทคนิคบนตารางที่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="afd14-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="afd14-127">เลือกชนิดข้อมูลสำหรับฟิลด์ใหม่</span><span class="sxs-lookup"><span data-stu-id="afd14-127">Select the data type for the new field.</span></span> <span data-ttu-id="afd14-128">ชนิดข้อมูลที่พร้อมใช้งานคือ กล่องกาเครื่องหมาย วันที่ วันที่และเวลา ทศนิยม หมายเลข รายการเบิกสินค้า และข้อความ</span><span class="sxs-lookup"><span data-stu-id="afd14-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="afd14-129">ถ้าคุณเลือกชนิดข้อมูลข้อความ คุณยังสามารถระบุความยาวสูงสุดของข้อความที่สามารถป้อนในฟิลด์นี้ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="afd14-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="afd14-130">ถ้าคุณเลือกชนิดข้อมูลรายการเบิกสินค้า คุณยังสามารถเลือกชุดของค่าที่ถูกต้องสำหรับฟิลด์ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="afd14-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="afd14-131">ระบุชื่อ ป้ายชื่อ และข้อความวิธีใช้สำหรับฟิลด์</span><span class="sxs-lookup"><span data-stu-id="afd14-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="afd14-132">ชื่อสอดคล้องกับชื่อฟิลด์ที่มีอยู่จริงในฐานข้อมูล ในขณะที่ข้อความป้ายชื่อและวิธีใช้เป็นข้อความที่ใช้เพื่อแสดงถึงฟิลด์นี้ในอินเทอร์เฟสผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="afd14-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="afd14-133">ถ้านี่เป็นเพียงฟิลด์เดียวที่คุณต้องการสร้างสำหรับแบบฟอร์มนี้ คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="afd14-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="afd14-134">ถ้าคุณต้องการสร้างฟิลด์เพิ่มเติม คลิก **บันทึก และสร้าง** และกลับไปยังขั้นตอนที่ 7</span><span class="sxs-lookup"><span data-stu-id="afd14-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="afd14-135">โปรดสังเกตว่า ขณะนี้ มีขีดจำกัดของฟิลด์ที่กำหนดเองเป็น **20 ฟิลด์ต่อตาราง**</span><span class="sxs-lookup"><span data-stu-id="afd14-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="afd14-136">การออกจากกล่องโต้ตอบ **สร้างฟิลด์ใหม่** จะนำคุณกลับไปยังกล่องโต้ตอบ **แทรกฟิลด์**</span><span class="sxs-lookup"><span data-stu-id="afd14-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="afd14-137">ฟิลด์ที่กำหนดเองใดๆ ที่เพิ่งถูกเพิ่ม จะสามารถถูกทำเครื่องหมายในรายการฟิลด์ที่จะแทรกลงในแบบฟอร์มได้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="afd14-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="afd14-138">คลิก **แทรก** เพื่อแทรกฟิลด์ที่ทำเครื่องหมายลงในพื้นที่ที่เลือกของแบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="afd14-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="afd14-139">**เลือกระบุได้:** เปิดใช้งานโหมด **ย้าย** จากแถบเครื่องมือการตั้งค่าส่วนบุคคล เพื่อย้ายฟิลด์ใหม่ไปยังตำแหน่งที่ต้องการของพวกเขาในพื้นที่ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="afd14-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="afd14-140">ดู [ปรับประสบการณ์ผู้ใช้ให้เป็นแบบส่วนบุคคล](personalize-user-experience.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ความสามารถในการตั้งค่าส่วนบุคคลต่างๆ เพื่อเพิ่มประสิทธิภาพแบบฟอร์มสำหรับการใช้งานส่วนบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="afd14-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="afd14-141">ใช้ฟิลด์ที่กำหนดเองร่วมกับผู้ใช้รายอื่น</span><span class="sxs-lookup"><span data-stu-id="afd14-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="afd14-142">หลังจากที่คุณสร้างฟิลด์แบบกำหนดเอง และแสดงในแบบฟอร์ม คุณอาจต้องการให้มุมมองหน้าที่มีการอัพเดตนี้ที่รวมฟิลด์ใหม่ให้ผู้ใช้อื่นๆ ในระบบ</span><span class="sxs-lookup"><span data-stu-id="afd14-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="afd14-143">ซึ่งสามารถทำได้ในสองวิธีที่แตกต่างกัน โดยใช้ความสามารถในการตั้งค่าส่วนบุคคลของผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="afd14-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="afd14-144">กระบวนการผลิตที่แนะนำคือ ผ่านผู้ดูแลระบบ ผู้ซึ่งสามารถกำหนดการตั้งค่าส่วนบุคคลให้กับผู้ใช้ทั้งหมดหรือชุดย่อยของผู้ใช้ได้</span><span class="sxs-lookup"><span data-stu-id="afd14-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="afd14-145">ดู [ปรับประสบการณ์ผู้ใช้เป็นแบบส่วนตัว](personalize-user-experience.md) สำหรับข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="afd14-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="afd14-146">อีกทางหนึ่งคือ คุณสามารถส่งออกการเปลี่ยนแปลงของคุณ (เรียกว่า *การตั้งค่าส่วนบุคคล*) ส่งไปยังผู้ใช้อย่างน้อยหนึ่งราย และให้ผู้ใช้ดังกล่าวแต่ละรายนำเข้าการเปลี่ยนแปลงของคุณ</span><span class="sxs-lookup"><span data-stu-id="afd14-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="afd14-147">ตัวเลือก **จัดการ** บนแถบเครื่องมือการตั้งค่าส่วนบุคคล ช่วยให้คุณสามารถส่งออกและนำเข้าการตั้งค่าส่วนบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="afd14-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="afd14-148">การจัดการฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-148">Managing custom fields</span></span>

<span data-ttu-id="afd14-149">การจัดการของฟิลด์ที่กำหนดเองทั้งหมดในระบบสามารถดำเนินการผ่านหน้า **ฟิลด์ที่กำหนดเอง** ในโมดูลการดูแลระบบได้</span><span class="sxs-lookup"><span data-stu-id="afd14-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="afd14-150">หน้านี้อนุญาตให้ผู้ใช้เข้าถึงความสามารถที่หลากหลาย ซึ่งรวมถึง:</span><span class="sxs-lookup"><span data-stu-id="afd14-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="afd14-151">การดูรายการของฟิลด์ที่กำหนดเองทั้งหมดในระบบ</span><span class="sxs-lookup"><span data-stu-id="afd14-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="afd14-152">การแก้ไขที่จำกัดของฟิลด์ที่กำหนดเองที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="afd14-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="afd14-153">การลบฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-153">Deleting custom fields.</span></span>
- <span data-ttu-id="afd14-154">การแสดงฟิลด์ที่กำหนดเองบนเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="afd14-155">การแสดงการแปลข้อความป้ายชื่อฟิลด์ที่กำหนดเองและข้อความวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="afd14-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="afd14-156">การดูฟิลด์ที่กำหนดเองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="afd14-156">Viewing all custom fields</span></span>

<span data-ttu-id="afd14-157">หน้า **ฟิลด์ที่กำหนดเอง** ให้ความสามารถในการมองเห็นฟิลด์แบบกำหนดเองทั้งหมดที่ได้ถูกกำหนดไว้ในระบบ</span><span class="sxs-lookup"><span data-stu-id="afd14-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="afd14-158">เพียงเลือกตารางที่คุณสนใจ และหน้าจะปรับปรุงเพื่อแสดงรายการของฟิลด์ที่กำหนดเองที่เชื่อมโยงกับตารางนั้น</span><span class="sxs-lookup"><span data-stu-id="afd14-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="afd14-159">การเลือกฟิลด์ที่กำหนดเองจากรายการจะช่วยให้คุณสามารถดูรายละเอียดเกี่ยวกับฟิลด์ได้</span><span class="sxs-lookup"><span data-stu-id="afd14-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="afd14-160">การแก้ไขฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-160">Editing custom fields</span></span>

<span data-ttu-id="afd14-161">หลังจากการสร้างฟิลด์แบบกำหนดเอง แล้วสามารถปรับเปลี่ยนได้เฉพาะข้อมูลบางรายการเกี่ยวกับฟิลด์ที่กำหนดเองในหน้า **ฟิลด์แบบกำหนดเอง** ได้</span><span class="sxs-lookup"><span data-stu-id="afd14-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="afd14-162">คุณ *สามารถ* ปรับเปลี่ยนแอททริบิวต์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="afd14-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="afd14-163">ป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="afd14-163">Label</span></span>
- <span data-ttu-id="afd14-164">ข้อความวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="afd14-164">Help text</span></span>
- <span data-ttu-id="afd14-165">ความยาว สำหรับฟิลด์ข้อความ</span><span class="sxs-lookup"><span data-stu-id="afd14-165">Length, for Text fields</span></span>

<span data-ttu-id="afd14-166">คุณ *ไม่สามารถ* แก้ไขแอททริบิวต์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="afd14-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="afd14-167">ชื่อฟิลด์</span><span class="sxs-lookup"><span data-stu-id="afd14-167">Field name</span></span>
- <span data-ttu-id="afd14-168">ชนิดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-168">Data type</span></span>

<span data-ttu-id="afd14-169">นอกจากนี้ สำหรับฟิลด์รายการเบิกสินค้า ชุดของค่าที่ถูกต้องสำหรับฟิลด์ที่กำหนดเองสามารถถูกจัดลำดับใหม่ และสามารถเพิ่มค่าใหม่ได้; อย่างไรก็ตาม ค่าที่มีอยู่สำหรับฟิลด์รายการเบิกสินค้าไม่สามารถถูกลบออกได้</span><span class="sxs-lookup"><span data-stu-id="afd14-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="afd14-170">คุณต้องคลิก **ใช้การเปลี่ยนแปลง** เมื่อคุณทำการแก้ไขฟิลด์เสร็จสิ้นสำหรับตารางที่ระบุ เพื่อบันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="afd14-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="afd14-171">การแสดงฟิลด์ที่กำหนดเองบนเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="afd14-172">นอกจากนี้ ยังเป็นสิ้งสำคัญในการอนุญาตให้สามารถมองเห็นฟิลด์ที่กำหนดเองได้บนเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="afd14-173">เอนทิตี้ข้อมูลจะถูกใช้ในคุณลักษณะ [ภาพรวมการรวม Office](../../dev-itpro/office-integration/office-integration.md) เช่นเดียวกับสำหรับสถานการณ์จำลองการนำเข้า/ส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="afd14-174">ทำตามขั้นตอนเหล่านี้เพื่อแสดงถึงฟิลด์ที่กำหนดเองบนเอนทิตี้ข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="afd14-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="afd14-175">เลือกฟิลด์ที่กำหนดเองในแบบฟอร์ม **ฟิลด์ที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="afd14-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="afd14-176">ขยายส่วน **เอนทิตี** เพื่อดูชุดของเอนทิตี้ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="afd14-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="afd14-177">คลิกปุ่ม **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="afd14-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="afd14-178">ปรับเปลี่ยนฟิลด์ **ถูกเปิดใช้งาน** ที่จะถูกเลือกสำหรับแต่ละเอนทิตี้ที่ควรแสดงฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="afd14-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="afd14-179">คลิก **บันทึกการเปลี่ยนแปลง** เพื่อบันทึกการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="afd14-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="afd14-180">การอนุญาตให้ฟิลด์ที่กำหนดเองถูกแสดงในภาษาอื่น</span><span class="sxs-lookup"><span data-stu-id="afd14-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="afd14-181">เนื่องจากฟิลด์ที่กำหนดเองอาจจำเป็นต้องสามารถเข้าถึงได้โดยผู้ใช้ในหลายภาษา หน้า **ฟิลด์ที่กำหนดเอง** มีกลไกเพื่ออนุญาตให้มีข้อความป้ายชื่อและวิธีใช้สำหรับฟิลด์ที่กำหนดเองที่จะถูกแปลเป็นภาษาอื่น</span><span class="sxs-lookup"><span data-stu-id="afd14-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="afd14-182">ขั้นตอนต่อไปนี้อธิบายกระบวนการสำหรับการแปลฟิลด์ที่กำหนดเองในภาษาอื่น:</span><span class="sxs-lookup"><span data-stu-id="afd14-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="afd14-183">เลือกฟิลด์ที่กำหนดเองในหน้า **ฟิลด์ที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="afd14-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="afd14-184">เลือกปุ่ม **การแปล** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="afd14-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="afd14-185">นี่จะเปิดเมนูแบบหล่นลงที่มีการแปลที่มีอยู่สำหรับฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="afd14-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="afd14-186">เมนูแบบหล่นลง **ภาษา** แสดงชุดของภาษาที่ได้มีการแปลไว้ให้เรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="afd14-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="afd14-187">ถ้าคุณต้องการแก้ไขการแปลที่มีอยู่ เลือกภาษาที่ต้องการจากเมนู และปรับเปลี่ยนค่าสำหรับป้ายชื่อ และข้อความวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="afd14-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="afd14-188">มิฉะนั้น คลิกปุ่ม **เพิ่มภาษา** เลือกภาษาที่ต้องการจากเมนู และจากนั้น ให้ค่าที่แปลสำหรับข้อความป้ายชื่อและวิธีใช้</span><span class="sxs-lookup"><span data-stu-id="afd14-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="afd14-189">คลิก **ตกลง** เมื่อคุณเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="afd14-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="afd14-190">การลบฟิลด์ที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="afd14-190">Deleting custom fields</span></span>

<span data-ttu-id="afd14-191">ในบางกรณี คุณอาจตัดสินใจว่าไม่ต้องการฟิลด์แบบกำหนดเองอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="afd14-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="afd14-192">เมื่อเหตุการณ์นี้เกิดขึ้น ผู้ดูแลระบบสามารถเลือกที่จะลบฟิลด์จากหน้า **ฟิลด์ที่กำหนดเอง** ได้</span><span class="sxs-lookup"><span data-stu-id="afd14-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="afd14-193">ในการทำเช่นนี้ ให้แน่ใจว่ามีการเลือกฟิลด์ที่ถูกต้อง คลิก **ลบ** คลิก **ใช่** เพื่อยืนยันการลบ และสุดท้ายคลิก **ใช้การเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="afd14-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="afd14-194">การดำเนินการนี้ไม่สามารถยกเลิกได้ และจะทำให้ข้อมูลที่เกี่ยวข้องกับฟิลด์ถูกลบออกอย่างถาวรจากฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="afd14-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="afd14-195">ภาคผนวก</span><span class="sxs-lookup"><span data-stu-id="afd14-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="afd14-196">ใครสามารถสร้างฟิลด์แบบกำหนดเองได้?</span><span class="sxs-lookup"><span data-stu-id="afd14-196">Who can create custom fields?</span></span>

<span data-ttu-id="afd14-197">เนื่องจากเป็นการป้องกันระบบ ผู้ดูแลระบบเท่านั้นจะสามารถสร้างฟิลด์แบบกำหนดเองได้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="afd14-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="afd14-198">อย่างไรก็ตาม ผู้ใช้ที่มีความชำนาญเหล่านั้นผู้ซึ่งองค์กรเห็นว่าจำเป็นจะได้รับสิทธิ์ในการสร้างฟิลด์แบบกำหนดเองโดยผู้ดูแลระบบ โดยใช้บทบาทความปลอดภัย **ผู้ใช้ที่มีความชำนาญแบบกำหนดเองสำหรับรันไทม์**</span><span class="sxs-lookup"><span data-stu-id="afd14-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="afd14-199">ผู้ใช้ที่ไม่มีบทบาทความปลอดภัยนี้จะไม่สามารถสร้างฟิลด์แบบกำหนดเองได้ แต่จะยังคงสามารถดูและโต้ตอบกับฟิลด์ที่กำหนดเองที่เพิ่มโดยผู้ใช้รายอื่นในระบบ</span><span class="sxs-lookup"><span data-stu-id="afd14-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="afd14-200">ตารางใดสนับสนุนฟิลด์ที่กำหนดเอง?</span><span class="sxs-lookup"><span data-stu-id="afd14-200">What tables support custom fields?</span></span>

<span data-ttu-id="afd14-201">สำหรับประสิทธิภาพและเหตุผลทางเทคนิค เฉพาะตารางที่ตรงตามเงื่อนไขต่อไปนี้ ในขณะนี้อนุญาตให้ใช้ฟิลด์แบบกำหนดเองที่จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="afd14-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="afd14-202">ตารางต้องมีการระบุป้ายเป็นหนึ่งในกลุ่มเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="afd14-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="afd14-203">กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="afd14-203">Group</span></span>
    - <span data-ttu-id="afd14-204">หัวข้อแผ่นงาน</span><span class="sxs-lookup"><span data-stu-id="afd14-204">WorksheetHeader</span></span>
    - <span data-ttu-id="afd14-205">หลัก</span><span class="sxs-lookup"><span data-stu-id="afd14-205">Main</span></span>
    - <span data-ttu-id="afd14-206">เบ็ดเตล็ด</span><span class="sxs-lookup"><span data-stu-id="afd14-206">Miscellaneous</span></span>
    - <span data-ttu-id="afd14-207">พารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="afd14-207">Parameter</span></span>
    - <span data-ttu-id="afd14-208">ข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="afd14-208">Reference</span></span>
    - <span data-ttu-id="afd14-209">หัวข้อธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="afd14-209">TransactionHeader</span></span>

- <span data-ttu-id="afd14-210">ตารางไม่สามารถขยายตารางอีกตารางได้</span><span class="sxs-lookup"><span data-stu-id="afd14-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="afd14-211">ตารางไม่สามารถถูกทำเครื่องหมายเป็นตารางระบบได้</span><span class="sxs-lookup"><span data-stu-id="afd14-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="afd14-212">ตารางไม่สามารถเป็นตารางชั่วคราวได้</span><span class="sxs-lookup"><span data-stu-id="afd14-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="afd14-213">ฉันสามารถอ้างอิงฟิลด์ที่กำหนดเองจากเครื่องมือสำหรับนักพัฒนาได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="afd14-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="afd14-214">สามารถจัดการฟิลด์ที่กำหนดเองโดยใช้อินเทอร์เฟซผู้ใช้เท่านั้น และไม่สามารถอ้างอิงโดยรหัสได้</span><span class="sxs-lookup"><span data-stu-id="afd14-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]