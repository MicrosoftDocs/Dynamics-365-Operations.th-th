---
title: ตั้งค่าพารามิเตอร์ของรูปแบบ ER สำหรับแต่ละนิติบุคคล
description: หัวข้อนี้อธิบายวิธีการตั้งค่าพารามิเตอร์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สำหรับแต่ละนิติบุคคล
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eebca6575a0b23f75baabbb91727f498de44d9cb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570721"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="4f777-103">ตั้งค่าพารามิเตอร์ของรูปแบบ ER สำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4f777-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4f777-104">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4f777-104">Prerequisites</span></span>

<span data-ttu-id="4f777-105">เมื่อต้องการดำเนินการตามขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการขั้นตอนในหัวข้อ [ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุไว้สำหรับแต่ละหัวข้อตามนิติบุคคล](er-app-specific-parameters-configure-format.md)</span><span class="sxs-lookup"><span data-stu-id="4f777-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="4f777-106">เมื่อต้องการดำเนินการตัวอย่างในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึง Microsoft Dynamics 365 Finance (การเงิน) สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4f777-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="4f777-107">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4f777-107">Electronic reporting developer</span></span>
- <span data-ttu-id="4f777-108">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4f777-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="4f777-109">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="4f777-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="4f777-110">นำเข้าการตั้งค่าคอนฟิกของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-110">Import ER configurations</span></span>

1.  <span data-ttu-id="4f777-111">ลงชื่อเข้าใช้สภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="4f777-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="4f777-112">บนแดชบอร์ดเริ่มต้น ให้เลือก **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4f777-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="4f777-113">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="4f777-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="4f777-114">นำเข้าไปยังอินสแตนซ์ปัจจุบันของ Finance การตั้งค่าคอนฟิกที่คุณส่งออกจาก Regulatory Configuration Services (RCS) ในขณะที่คุณกำลังดำเนินการขั้นตอนในหัวข้อ [ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุไว้สำหรับแต่ละหัวข้อตามนิติบุคคล](er-app-specific-parameters-configure-format.md)</span><span class="sxs-lookup"><span data-stu-id="4f777-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="4f777-115">ให้ทำตามขั้นตอนต่อไปนี้สำหรับการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) แต่ละรายการ ตามลำดับต่อไปนี้: รูปแบบข้อมูล การแม็ปแบบจำลอง และรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="4f777-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="4f777-116">เลือก **แลกเปลี่ยน \> โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="4f777-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="4f777-117">เลือก **เรียกดู** เพื่อเลือกไฟล์สำหรับการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="4f777-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="4f777-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-118">Select **OK**.</span></span>
    
    <span data-ttu-id="4f777-119">ภาพประกอบต่อไปนี้แสดงการตั้งค่าคอนฟิกที่คุณต้องมีเมื่อเสร็จสิ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="4f777-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![หน้าการตั้งค่าคอนฟิก ER](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="4f777-121">ตั้งค่าพารามิเตอร์สำหรับบริษัท DEMF</span><span class="sxs-lookup"><span data-stu-id="4f777-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="4f777-122">คุณสามารถใช้กรอบงาน ER ในการตั้งค่าพารามิเตอร์เฉพาะของแอพลิเคชันสำหรับรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="4f777-123">เลือกนิติบุคคล **DEMF**</span><span class="sxs-lookup"><span data-stu-id="4f777-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="4f777-124">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="4f777-125">ในบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **พารามิเตอร์เฉพาะของแอพลิเคชัน** เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="4f777-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="4f777-127">บนเพจ **พารามิเตอร์เฉพาะของแอพลิเคชัน** คุณสามารถตั้งค่าคอนฟิกกฎสำหรับแหล่งข้อมูล **ตัวเลือก** ของรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="4f777-128">ถ้ารูปแบบของ ER พื้นฐานประกอบด้วยแหล่งข้อมูลที่มีชนิด **การค้นหา** หลายแหล่ง คุณต้องเลือกแหล่งข้อมูลที่ต้องการบนแท็บด่วน **การค้นหา** ก่อนที่คุณจะสามารถเริ่มต้นการตั้งค่าคอนฟิกชุดของกฎสำหรับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="4f777-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="4f777-129">สำหรับแต่ละแหล่งข้อมูล คุณสามารถตั้งค่าคอนฟิกกฎแยกต่างหากสำหรับแต่ละรุ่นของรูปแบบของ ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4f777-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="4f777-130">ชุดของกฎทั้งหมดสำหรับแหล่งข้อมูลการค้นหาทั้งหมดที่พร้อมใช้งานในรูปแบบของ ER พื้นฐานของรุ่นที่เลือกสร้างพารามิเตอร์เฉพาะของแอพลิเคชันสำหรับรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="4f777-131">เลือกรุ่น **1.1.1** ของรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="4f777-132">บนแท็บด่วน **เงื่อนไข** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="4f777-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="4f777-133">ในฟิลด์ **รหัส** ของเรกคอร์ดใหม่ ให้เลือกลูกศรแบบหล่นลง เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4f777-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="4f777-134">การค้นหาจะแสดงรายการรหัสภาษีสำหรับการเลือก</span><span class="sxs-lookup"><span data-stu-id="4f777-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="4f777-135">รายการนี้จะถูกส่งคืนโดยแหล่งข้อมูล **Model.Data.Tax** ที่ได้รับการตั้งค่าคอนฟิกในรูปแบบของ ER พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="4f777-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="4f777-136">เนื่องจากแหล่งข้อมูลนี้มีฟิลด์ **ชื่อ** ชื่อของรหัสภาษีแต่ละรหัสจะปรากฏในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4f777-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="4f777-138">เลือกรหัสภาษี **VAT19**</span><span class="sxs-lookup"><span data-stu-id="4f777-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="4f777-139">ในฟิลด์ **ผลลัพธ์การค้นหา** ของเรกคอร์ดใหม่ ให้เลือกลูกศรแบบหล่นลง เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4f777-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="4f777-140">การค้นหาจะแสดงรายการของค่าสำหรับการแจงนับรูปแบบ TaxationLevel สำหรับการเลือก</span><span class="sxs-lookup"><span data-stu-id="4f777-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="4f777-141">โปรดทราบว่า ถ้าภาษาเยอรมันถูกเลือกเป็นภาษาที่ต้องการของผู้ใช้ที่คุณลงชื่อเข้าใช้ ป้ายชื่อของค่าในการค้นหาจะอยู่ในภาษาเยอรมัน ซึ่งระบุว่ามีการแปลในรูปแบบของ ER พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="4f777-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="4f777-142">นอกจากนี้ ถ้ามีการแปลป้ายชื่อของแหล่งข้อมูลการค้นหา ป้ายชื่อนั้นจะปรากฏขึ้นในภาษาที่ต้องการของผู้ใช้ในแท็บ **การค้นหา**</span><span class="sxs-lookup"><span data-stu-id="4f777-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="4f777-144">เลือกค่า **ภาษีปกติ**</span><span class="sxs-lookup"><span data-stu-id="4f777-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="4f777-145">โดยการเพิ่มเรกคอร์ดนี้ คุณกำหนดกฎต่อไปนี้: เมื่อใดก็ตามที่มีการร้องขอแหล่งข้อมูลการค้นหา **ตัวเลือก** และรหัสภาษี **VAT19** ถูกส่งผ่านไปเป็นอาร์กิวเมนต์ **ภาษีปกติ** จะถูกส่งคืนเป็นระดับภาษีที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="4f777-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="4f777-146">เลือก **เพิ่ม** แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-147">ในฟิลด์ **รหัส** ให้เลือกรหัสภาษี **InVAT19**</span><span class="sxs-lookup"><span data-stu-id="4f777-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="4f777-148">ในฟิลด์ **ผลลัพธ์การค้นหา**  ให้เลือกค่า **ภาษีปกติ**</span><span class="sxs-lookup"><span data-stu-id="4f777-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="4f777-149">เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-150">ในฟิลด์ **รหัส** ให้เลือกรหัสภาษี **VAT7**</span><span class="sxs-lookup"><span data-stu-id="4f777-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="4f777-151">ในฟิลด์ **ผลลัพธ์การค้นหา** ให้เลือกค่า **ภาษีที่ลดลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="4f777-152">เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-153">ในฟิลด์ **รหัส** ให้เลือกรหัสภาษี **InVAT7**</span><span class="sxs-lookup"><span data-stu-id="4f777-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="4f777-154">ในฟิลด์ **ผลลัพธ์การค้นหา** ให้เลือกค่า **ภาษีที่ลดลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="4f777-155">เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-156">ในฟิลด์ **รหัส** ให้เลือกรหัสภาษี **THIRD**</span><span class="sxs-lookup"><span data-stu-id="4f777-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="4f777-157">ในฟิลด์ **ผลลัพธ์การค้นหา** ให้เลือกค่า **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="4f777-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="4f777-158">เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-159">ในฟิลด์ **รหัส** ให้เลือกรหัสภาษี **InVAT0**</span><span class="sxs-lookup"><span data-stu-id="4f777-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="4f777-160">ในฟิลด์ **ผลลัพธ์การค้นหา** ให้เลือกค่า **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="4f777-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="4f777-161">เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="4f777-162">ในฟิลด์ **รหัส** ให้เลือกตัวเลือก **\*ไม่ว่างเปล่า\***</span><span class="sxs-lookup"><span data-stu-id="4f777-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="4f777-163">ในฟิลด์ **ผลลัพธ์การค้นหา** ให้เลือกค่า **อื่น**</span><span class="sxs-lookup"><span data-stu-id="4f777-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="4f777-164">โดยการเพิ่มเรกคอร์ดสุดท้ายนี้ คุณกำหนดกฎต่อไปนี้: เมื่อใดก็ตามที่รหัสภาษีที่ส่งผ่านเป็นอาร์กิวเมนต์ไม่เป็นไปตามกฎก่อนหน้านี้ แหล่งข้อมูลการค้นหาจะถูกส่งคืน **อื่นๆ** เป็นระดับภาษีที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="4f777-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="4f777-166">ในฟิลด์ **สถานะ** เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="4f777-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="4f777-167">เมื่อคุณรันรุ่นของรูปแบบของ ER ที่มีสถานะเป็น **เสร็จสมบูรณ์** หรือ **ใช้ร่วมกัน** ชุดของกฎนี้ต้องอยู่ในสถานะ **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="4f777-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="4f777-168">มิฉะนั้น การดำเนินการของรูปแบบของ ER พื้นฐานจะถูกขัดจังหวะ เมื่อรูปแบบพยายามโหลดข้อมูลจากชุดของกฎนี้ในขณะที่มีการรันแหล่งข้อมูลการค้นหา **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="4f777-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="4f777-169">เมื่อคุณรันรุ่นของรูปแบบของ ER ที่มีสถานะเป็น **ร่าง** รูปแบบของ ER พื้นฐานสามารถเข้าถึงชุดกฎนี้ได้ โดยไม่คำนึงถึงสถานะ</span><span class="sxs-lookup"><span data-stu-id="4f777-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="4f777-170">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4f777-170">Select **Save**.</span></span>
18. <span data-ttu-id="4f777-171">ปิดเพจ **พารามิเตอร์เฉพาะของแอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="4f777-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="4f777-172">รันรูปแบบของ ER ในบริษัท DEMF</span><span class="sxs-lookup"><span data-stu-id="4f777-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="4f777-173">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="4f777-174">บนบานหน้าต่างการดำเนินการ เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="4f777-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="4f777-175">ในกล่องโต้ตอบที่ปรากฏ เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="4f777-176">ดาวน์โหลดใบแจ้งยอดที่สร้างขึ้นและจัดเก็บไว้เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="4f777-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="4f777-177">ในใบแจ้งยอดที่สร้าง ให้สังเกตว่าสรุปของรหัสภาษี **InVAT7** ถูกวางในระดับ **ที่ลดลง** และสรุปของรหัสภาษี **VAT19** และ **InVA19** ถูกวางในระดับ **ปกติ**</span><span class="sxs-lookup"><span data-stu-id="4f777-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="4f777-178">ลักษณะการทำงานนี้จะขึ้นอยู่กับการตั้งค่าคอนฟิกในชุดของกฎนิติบุคคล–ไม่เป็นอิสระ</span><span class="sxs-lookup"><span data-stu-id="4f777-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="4f777-179">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีขาย \> รหัสภาษีขาย**</span><span class="sxs-lookup"><span data-stu-id="4f777-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="4f777-180">เลือกรหัสภาษี **InVAT7**</span><span class="sxs-lookup"><span data-stu-id="4f777-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="4f777-181">บนบานหน้าต่างการดำเนินการ บนแท็บ **รหัสภาษีขาย** ในกลุ่ม **การสอบถาม** ให้เลือก **ภาษีขายที่ลงรายการบัญชี** เพื่อดูข้อมูลเกี่ยวกับมูลค่าภาษีและอัตราภาษีที่ใช้สำหรับแต่ละรหัสภาษี</span><span class="sxs-lookup"><span data-stu-id="4f777-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![หน้าภาษีขายที่ลงรายการบัญชี](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="4f777-183">ปิดเพจภาษีขายที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4f777-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="4f777-184">ตั้งค่าพารามิเตอร์สำหรับบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="4f777-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="4f777-185">เลือกนิติบุคคล **USMF**</span><span class="sxs-lookup"><span data-stu-id="4f777-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="4f777-186">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="4f777-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="4f777-187">ในแผนภูมิการตั้งค่าคอนฟิก ขยายรายการ **แบบจำลองเพื่อเรียนรู้การโทรที่มีการกำหนดพารามิเตอร์** ขยายรายการ **รูปแบบเพื่อเรียนรู้การโทรที่มีการกำหนดพารามิเตอร์** และเลือก **รูปแบบเพื่อเรียนรู้วิธีการค้นหารูปแบบข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="4f777-188">ในบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **พารามิเตอร์เฉพาะของแอพลิเคชัน** เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="4f777-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="4f777-189">เลือกรุ่น **1.1.1** ของรูปแบบของ ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4f777-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="4f777-190">บนแท็บด่วน **เงื่อนไข** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="4f777-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="4f777-191">ในฟิลด์ **รหัส** ของเรกคอร์ดใหม่ ให้เลือกลูกศรแบบหล่นลง เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4f777-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="4f777-192">การค้นหาในปัจจุบันแสดงรายการรหัสภาษีสำหรับการเลือกภาษีบริษัท **USMF**</span><span class="sxs-lookup"><span data-stu-id="4f777-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="4f777-194">เลือกรหัสภาษี **EXEMPT**</span><span class="sxs-lookup"><span data-stu-id="4f777-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="4f777-195">ในฟิลด์ **ผลลัพธ์การค้นหา** ของเรกคอร์ดใหม่ ให้เลือกค่า **ไม่มีภาษี**</span><span class="sxs-lookup"><span data-stu-id="4f777-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="4f777-196">เลือก **เพิ่ม** อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4f777-196">Select **Add** again.</span></span>
11. <span data-ttu-id="4f777-197">ในฟิลด์ **รหัส** ของเรกคอร์ดใหม่ ให้เลือกตัวเลือก **\*ไม่ว่างเปล่า\***</span><span class="sxs-lookup"><span data-stu-id="4f777-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="4f777-198">ในฟิลด์ **ผลลัพธ์การค้นหา** ของเรกคอร์ดใหม่ ให้เลือกค่า **ภาษีปกติ**</span><span class="sxs-lookup"><span data-stu-id="4f777-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="4f777-199">ในฟิลด์ **สถานะ** เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="4f777-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="4f777-200">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4f777-200">Select **Save**.</span></span>

    ![เพจพารามิเตอร์เฉพาะของแอพลิเคชันของ ER](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="4f777-202">ปิดเพจ **พารามิเตอร์เฉพาะของแอพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="4f777-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="4f777-203">รันรูปแบบของ ER ในบริษัท USMF</span><span class="sxs-lookup"><span data-stu-id="4f777-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="4f777-204">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="4f777-205">บนบานหน้าต่างการดำเนินการ เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="4f777-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="4f777-206">ในกล่องโต้ตอบที่ปรากฏ เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="4f777-207">ดาวน์โหลดใบแจ้งยอดที่สร้างขึ้นและจัดเก็บไว้เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="4f777-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="4f777-208">ในใบแจ้งยอดที่สร้าง ให้สังเกตว่าขณะนี้คุณได้นำรูปแบบของ ER เดียวกันมาใช้ใหม่ สำหรับนิติบุคคลที่แตกต่าง แต่ไม่มีการปรับปรุงใดๆ ให้กับรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="4f777-209">ใช้พารามิเตอร์นิติบุคคล–ไม่เป็นอิสระอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="4f777-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="4f777-210">พารามิเตอร์การส่งออก</span><span class="sxs-lookup"><span data-stu-id="4f777-210">Export parameters</span></span>

1.  <span data-ttu-id="4f777-211">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4f777-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="4f777-212">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="4f777-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="4f777-213">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรูปแบบ **รูปแบบเพื่อเรียนรู้วิธีการค้นหาข้อมูล LE**</span><span class="sxs-lookup"><span data-stu-id="4f777-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="4f777-214">ในบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **พารามิเตอร์เฉพาะของแอพลิเคชัน** เลือก **ตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="4f777-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="4f777-215">เลือกรุ่น **1.1.1** ของรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="4f777-216">ในบานหน้าต่างการดำเนินการ เลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="4f777-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="4f777-217">ดาวน์โหลดไฟล์ที่สร้างขึ้นและจัดเก็บไว้เฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="4f777-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="4f777-218">ขณะนี้ มีการส่งออกชุดของพารามิเตอร์เฉพาะของแอพลิเคชันที่ตั้งค่าคอนฟิกเป็นไฟล์ XML แล้ว</span><span class="sxs-lookup"><span data-stu-id="4f777-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="4f777-219">พารามิเตอร์การนำเข้า</span><span class="sxs-lookup"><span data-stu-id="4f777-219">Import parameters</span></span>

1.  <span data-ttu-id="4f777-220">เลือกรุ่น **1.1.2** ของรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="4f777-221">ในบานหน้าต่างการดำเนินการ เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="4f777-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="4f777-222">เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการแทนที่พารามิเตอร์เฉพาะของแอพลิเคชันที่มีอยู่สำหรับรุ่นของรูปแบบนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="4f777-223">เลือก **เรียกดู** เพื่อค้นหาไฟล์ที่มีพารามิเตอร์เฉพาะของแอพลิเคชันที่ส่งออกสำหรับรุ่น **1.1.1**</span><span class="sxs-lookup"><span data-stu-id="4f777-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="4f777-224">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4f777-224">Select **OK**.</span></span>

    <span data-ttu-id="4f777-225">รุ่น **1.1.2** ของรูปแบบของ ER ในปัจจุบันมีพารามิเตอร์เฉพาะของแอพลิเคชันเดียวกันกับที่คุณได้ตั้งค่าคอนฟิกไว้สำหรับ **1.1.1** ครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="4f777-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="4f777-226">โปรดทราบว่าพารามิเตอร์เฉพาะของแอพลิเคชันของรูปแบบของ ER มีนิติบุคคล–ไม่เป็นอิสระ</span><span class="sxs-lookup"><span data-stu-id="4f777-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="4f777-227">เมื่อต้องการใช้ซ้ำพารามิเตอร์เฉพาะของแอพลิเคชันที่ได้รับการตั้งค่าคอนฟิกสำหรับนิติบุคคลหนึ่งในนิติบุคคลที่แตกต่างกัน คุณต้องส่งออกในระหว่างที่คุณลงชื่อเข้าใช้นิติบุคคลแรก แล้วนำเข้าข้อมูลดังกล่าวหลังจากที่คุณลงชื่อเข้าใช้ไปยังนิติบุคคลอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4f777-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="4f777-228">นอกจากนี้คุณยังสามารถใช้วิธีการนี้ในการโอนย้ายรูปแบบของ ER ที่เกี่ยวข้องกับพารามิเตอร์เฉพาะของแอพลิเคชันที่มีการตั้งค่าคอนฟิกในครั้งแรกในอินสแตนซ์หนึ่งของ Finance กับอินสแตนซ์อื่นของ Finance</span><span class="sxs-lookup"><span data-stu-id="4f777-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="4f777-229">โปรดทราบว่าถ้าคุณตั้งค่าคอนฟิกพารามิเตอร์เฉพาะของแอพลิเคชันสำหรับรูปแบบของ ER รุ่นเดียว และนำเข้ารุ่นที่สูงกว่าของรูปแบบเดียวกันไปยังอินสแตนซ์ Finance ปัจจุบัน จะไม่มีการใช้พารามิเตอร์เฉพาะของแอพลิเคชันที่มีอยู่สำหรับรุ่นที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="4f777-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="4f777-230">นอกจากนี้ควรตระหนักว่าเมื่อคุณเลือกไฟล์สำหรับการนำเข้า โครงสร้างของพารามิเตอร์เฉพาะของแอพลิเคชันในไฟล์นั้นจะถูกเปรียบเทียบกับโครงสร้างของแหล่งข้อมูลที่เกี่ยวข้องของชนิด **การค้นหา** ในรูปแบบของ ER ที่เลือกสำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="4f777-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="4f777-231">การนำเข้าจะเสร็จเมื่อโครงสร้างของพารามิเตอร์เฉพาะของแอพลิเคชันแต่ละพารามิเตอร์ตรงกับโครงสร้างของแหล่งข้อมูลที่สอดคล้องกันในรูปแบบของ ER ซึ่งเลือกไว้สำหรับการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="4f777-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="4f777-232">ถ้าโครงสร้างไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือนที่ระบุว่าไม่สามารถดำเนินการนำเข้าได้</span><span class="sxs-lookup"><span data-stu-id="4f777-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="4f777-233">ถ้าคุณบังคับให้มีการดำเนินการนำเข้า พารามิเตอร์เฉพาะของแอพลิเคชันที่มีอยู่สำหรับรูปแบบของ ER ที่เลือกไว้จะได้รับการล้างข้อมูล และคุณต้องตั้งค่าจากจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="4f777-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="4f777-234">ความสัมพันธ์ระหว่างพารามิเตอร์เฉพาะของแอพลิเคชันและรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="4f777-235">ความสัมพันธ์ระหว่างรูปแบบของ ER และพารามิเตอร์เฉพาะของแอพลิเคชันจะถูกสร้างโดยรหัสการระบุที่ไม่ซ้ำกันสำหรับอินสแตนซ์ของรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="4f777-236">ดังนั้น เมื่อคุณลบรูปแบบของ ER จาก Finance พารามิเตอร์เฉพาะของแอพลิเคชันที่มีการตั้งค่าคอนฟิกสำหรับรูปแบบของ ER จะถูกเก็บไว้ในอินสแตนซ์ปัจจุบันของ Finance</span><span class="sxs-lookup"><span data-stu-id="4f777-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="4f777-237">ผู้ใช้สามารถเข้าถึงเมื่อใดก็ได้ที่มีการนำเข้ารูปแบบของ ER พื้นฐานอีกครั้งเข้ากับอินสแตนซ์ของ Finance</span><span class="sxs-lookup"><span data-stu-id="4f777-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="4f777-238">เข้าถึงพารามิเตอร์เฉพาะของแอพลิเคชันโดยใช้กรอบงานของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="4f777-239">ในตัวอย่างก่อนหน้านี้ คุณสามารถเข้าถึงพารามิเตอร์เฉพาะแอพลิเคชันของรูปแบบของ ER โดยการใช้กรอบงานของ ER</span><span class="sxs-lookup"><span data-stu-id="4f777-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="4f777-240">วิธีการนี้ไม่อนุญาตให้คุณจำกัดการเข้าถึงพารามิเตอร์เฉพาะของแอพลิเคชันของรูปแบบของ ER เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4f777-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="4f777-241">ถ้าคุณต้องใช้ข้อจำกัดดังกล่าว ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="4f777-242">ใช้รายการเมนู **ERSolutionAppSpecificParametersDesigner** ที่มีอยู่ใหม่ หรือใช้รายการเมนู **ERSolutionAppSpecificParametersDesigner** ของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="4f777-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![เพจ Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="4f777-244">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="4f777-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="4f777-245">สร้างปุ่มรายการเมนูใหม่ และเชื่อมโยงไปยังเรกคอร์ดที่เกี่ยวข้องจากตาราง **ERSolutionTable** โดยตั้งค่าคุณสมบัติ **แหล่งข้อมูล** เป็น **ERSolutionTable**</span><span class="sxs-lookup"><span data-stu-id="4f777-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![เพจ Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="4f777-247">สร้างปุ่มแบบง่าย และแทนที่วิธีการ **คลิก** ดังที่แสดงในตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="4f777-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="4f777-248">การใช้วิธีการนี้ คุณจะสามารถระบุรหัสโซลูชันที่ไม่ซ้ำกัน (ที่กำหนดโดยใช้ค่า **GUID**) เพื่ออนุญาตให้เข้าถึงพารามิเตอร์เฉพาะของแอพลิเคชันได้เฉพาะกับรูปแบบของ ER เฉพาะ และสำเนาสืบทอดที่ได้รับมา</span><span class="sxs-lookup"><span data-stu-id="4f777-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="4f777-249">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4f777-249">Additional resources</span></span>

[<span data-ttu-id="4f777-250">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4f777-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4f777-251">ตั้งค่าคอนฟิกรูปแบบ ER เพื่อใช้พารามิเตอร์ที่ระบุสำหรับแต่ละนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="4f777-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]