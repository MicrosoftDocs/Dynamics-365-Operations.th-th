---
title: "FAQ เกี่ยวกับการแปลที่เกี่ยวข้องกับผลิตภัณฑ์"
description: "หัวข้อนี้อธิบายวิธีการจัดการการแปลสำหรับผลิตภัณฑ์ ค่ามิติของผลิตภัณฑ์ และคุณลักษณะของผลิตภัณฑ์"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b5e06d7928f1ad794eed1c4cb6d2d93d87e30066
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="product-related-translations-faq"></a><span data-ttu-id="a44eb-103">FAQ เกี่ยวกับการแปลที่เกี่ยวข้องกับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a44eb-103">Product-related translations FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a44eb-104">หัวข้อนี้อธิบายวิธีการจัดการการแปลสำหรับผลิตภัณฑ์ ค่ามิติของผลิตภัณฑ์ และคุณลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a44eb-104">This topic describes how to manage translations for products, product dimension values, and product attributes.</span></span> 

<a name="what-product-related-data-can-be-translated"></a><span data-ttu-id="a44eb-105">สามารถแปลข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a44eb-105">What product-related data can be translated?</span></span>
--------------------------------------------

<span data-ttu-id="a44eb-106">คุณสามารถสร้างการแปลสำหรับข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-106">You can create translations for the following product-related information:</span></span>
-   <span data-ttu-id="a44eb-107">ชื่อและคำอธิบายของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a44eb-107">Names and descriptions of products.</span></span>
-   <span data-ttu-id="a44eb-108">คำอธิบาย ชื่อที่เข้าใจง่าย และข้อความวิธีใช้ของค่าคุณลักษณะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a44eb-108">Descriptions, friendly names, and help text of product attribute values.</span></span>
-   <span data-ttu-id="a44eb-109">ชื่อและคำอธิบายของค่ามิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a44eb-109">Names and descriptions of product dimension values.</span></span>

<span data-ttu-id="a44eb-110">คุณสามารถแปลข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์เป็นภาษาใดๆ ที่มีอยู่ในหน้า **การแปลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-110">You can translate the product-related information into any language that is available from the **Text translation** page.</span></span> <span data-ttu-id="a44eb-111">สำหรับข้อมูลเพิ่มเติม ให้ดูส่วนต่อไปนี้ **ฉันจะสร้างคำแปลสำหรับข้อมูลเกี่ยวกับผลิตภัณฑ์ได้อย่างไร**</span><span class="sxs-lookup"><span data-stu-id="a44eb-111">For more information, see the following section **How do I created translations for product-related information**.</span></span>

## <a name="where-can-i-view-the-translated-information"></a><span data-ttu-id="a44eb-112">ฉันสามารถดูข้อมูลการแปลได้ที่ไหน</span><span class="sxs-lookup"><span data-stu-id="a44eb-112">Where can I view the translated information?</span></span>
<span data-ttu-id="a44eb-113">คุณสามารถดูการแปลข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์ในเอกสารต้นทางภายนอก เช่น ใบแจ้งหนี้ ที่ใช้ภาษาที่แปลพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a44eb-113">You can view translations of product-related information in any external source document, such as an invoice, that uses a language where translations are available.</span></span>

## <a name="how-do-i-create-translations-for-product-related-information"></a><span data-ttu-id="a44eb-114">ฉันสร้างการแปลสำหรับข้อมูลเกี่ยวกับผลิตภัณฑ์ได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="a44eb-114">How do I create translations for product-related information?</span></span>
<span data-ttu-id="a44eb-115">เมื่อต้องการสร้างการแปลสำหรับผลิตภัณฑ์ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-115">To create translations for a product, follow these steps:</span></span>
1.  <span data-ttu-id="a44eb-116">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ทั่วไป** &gt; **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a44eb-116">Click **Product information management** &gt; **Common** &gt; **Released products**.</span></span>
2.  <span data-ttu-id="a44eb-117">เลือกผลิตภัณฑ์ และบน บานหน้าต่างการดำเนินการในกลุ่ม **ภาษา** ให้คลิก **การแปล**</span><span class="sxs-lookup"><span data-stu-id="a44eb-117">Select a product, and on the Action Pane, in the **Languages** group, click **Translations**.</span></span>
3.  <span data-ttu-id="a44eb-118">ในหน้า **การแปลข้อความ** ในฟิลด์ **ภาษา** เลือกภาษา</span><span class="sxs-lookup"><span data-stu-id="a44eb-118">In the **Text translation** page, in the **Language** field, select a language.</span></span> <span data-ttu-id="a44eb-119">เมื่อต้องการเพิ่มภาษา ให้ขยายฟิลด์ **ภาษา** และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a44eb-119">To add more languages, expand the **Language** field, and then click **OK**.</span></span>
4.  <span data-ttu-id="a44eb-120">ในกลุ่ม **ข้อความที่แปลแล้ว** ให้ป้อนคำแปลในฟิลด์ **คำอธิบาย** และ **ชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="a44eb-120">In the **Translated text** group, enter translations in the **Description** and **Product name** fields.</span></span>

<span data-ttu-id="a44eb-121">เมื่อต้องการสร้างการแปลสำหรับคุณลักษณะของผลิตภัณฑ์ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-121">To create translations for product attributes, follow these steps:</span></span>
1.  <span data-ttu-id="a44eb-122">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ทั่วไป** &gt; **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a44eb-122">Click **Product information management** &gt; **Common** &gt; **Released products**.</span></span>
2.  <span data-ttu-id="a44eb-123">ภายใต้ **การตั้งค่า**คลิก **แอททริบิวต์**แล้วคลิก **แอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="a44eb-123">Under **Setup**, click **Attributes**, and then click **Attributes**.</span></span>
3.  <span data-ttu-id="a44eb-124">ในหน้า **แอททริบิวต์** คลิก **แปล**</span><span class="sxs-lookup"><span data-stu-id="a44eb-124">In the **Attributes** page, click **Translate**.</span></span>
4.  <span data-ttu-id="a44eb-125">ในหน้า **การแปลข้อความ** ในฟิลด์ **ภาษา** เลือกภาษา</span><span class="sxs-lookup"><span data-stu-id="a44eb-125">In the **Text translation** page, in the **Language** field, select a language.</span></span> <span data-ttu-id="a44eb-126">เมื่อต้องการเพิ่มภาษา ให้ขยายฟิลด์ **ภาษา** และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a44eb-126">To add more languages, expand the **Language** field, and then click **OK**.</span></span>
5.  <span data-ttu-id="a44eb-127">ในกลุ่ม **ข้อความที่แปลแล้ว** ให้ป้อนคำแปลในฟิลด์ **คำอธิบาย** **ชื่อที่จำง่าย**และ **ข้อความวิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="a44eb-127">In the **Translated text** group, enter translations in the **Description**, **Friendly name**, and **Help text** fields.</span></span>

<span data-ttu-id="a44eb-128">เมื่อต้องการสร้างการแปลสำหรับสำหรับค่ามิติของผลิตภัณฑ์ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-128">To create translations for product dimension values, follow these steps:</span></span>
1.  <span data-ttu-id="a44eb-129">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **ทั่วไป** &gt; **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="a44eb-129">Click **Product information management** &gt; **Common** &gt; **Released products**.</span></span>
2.  <span data-ttu-id="a44eb-130">เลือกผลิตภัณฑ์ แล้วคลิก **มิติของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="a44eb-130">Select a product, and then click **Product dimensions**.</span></span>
3.  <span data-ttu-id="a44eb-131">เลือกตัวเลือกอย่างใดอย่างหนึ่งของการเชื่อมโยงสำหรับมิติของผลิตภัณฑ์: **การตั้งค่าคอนฟิก** **ขนาด** **สี**หรือ **ลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-131">Select one of the links for the product dimensions: **Configurations**, **Sizes**, **Colors**, or **Style**.</span></span>
4.  <span data-ttu-id="a44eb-132">เลือกค่ามิติทางการเงิน และจากนั้น คลิก **แปล**</span><span class="sxs-lookup"><span data-stu-id="a44eb-132">Select a dimension value and then click **Translate**.</span></span>
5.  <span data-ttu-id="a44eb-133">ในหน้า **การแปลข้อความ** ในฟิลด์ **ภาษา** เลือกภาษา</span><span class="sxs-lookup"><span data-stu-id="a44eb-133">In the **Text translation** page, in the **Language** field, select a language.</span></span> <span data-ttu-id="a44eb-134">เมื่อต้องการเพิ่มภาษา ให้ขยายฟิลด์ **ภาษา** และจากนั้นคลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a44eb-134">To add more languages, expand the **Language** field, and then click **OK**.</span></span>
6.  <span data-ttu-id="a44eb-135">ในกลุ่ม **ข้อความที่แปลแล้ว** ให้ป้อนคำแปลในฟิลด์ **ชื่อ** และ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a44eb-135">In the **Translated text** group, enter translations in the **Name** and **Description** fields.</span></span>

## <a name="can-the-names-of-product-variants-be-translated"></a><span data-ttu-id="a44eb-136">สามารถแปลชื่อผลิตภัณฑ์ย่อยได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="a44eb-136">Can the names of product variants be translated?</span></span>
<span data-ttu-id="a44eb-137">ผลิตภัณฑ์ย่อยขึ้นอยู่กับมิติของผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="a44eb-137">Product variants are based on the dimensions of a released product.</span></span> <span data-ttu-id="a44eb-138">ชื่อผลิตภัณฑ์ย่อยขึ้นอยู่กับชุดของค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="a44eb-138">Product variant names are based on a combination of dimension values.</span></span> <span data-ttu-id="a44eb-139">เมื่อมีการแปลค่ามิติที่เกี่ยวข้องกับผลิตภัณฑ์ย่อย ชื่อของผลิตภัณฑ์ย่อยจะปรากฏขึ้นในเวอร์ชันที่แปลแล้ว</span><span class="sxs-lookup"><span data-stu-id="a44eb-139">When the dimension values that are associated with a product variant are translated, the name of the product variant appears in the translated version.</span></span>  

<span data-ttu-id="a44eb-140">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a44eb-140">**Example**</span></span>  

<span data-ttu-id="a44eb-141">ผลิตภัณฑ์ของคุณคือเสื้อยืดคอกลมที่มีขนาดและสีแตกต่างกัน และชื่อย่อยจะขึ้นอยู่กับรายละเอียดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-141">Your product is a T-shirt that comes in different sizes and colors and the variant names are based on the following details:</span></span>
-   <span data-ttu-id="a44eb-142">หมายเลขผลิตภัณฑ์: \#3</span><span class="sxs-lookup"><span data-stu-id="a44eb-142">Product number: \#3</span></span>
-   <span data-ttu-id="a44eb-143">มิติ: ขนาดและสี</span><span class="sxs-lookup"><span data-stu-id="a44eb-143">Dimensions: Size and color</span></span>
-   <span data-ttu-id="a44eb-144">ค่ามิติขนาด: ขนาดเล็ก ปานกลาง ขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="a44eb-144">Size dimension values: Small, Medium, Large</span></span>
-   <span data-ttu-id="a44eb-145">ค่ามิติสี: สีแดง สีเขียว สีดำ</span><span class="sxs-lookup"><span data-stu-id="a44eb-145">Color dimension values: Red, Green, Black</span></span>

<span data-ttu-id="a44eb-146">ชื่อของผลิตภัณฑ์ย่อยที่ยึดตามมิติค่าขนาดเล็ก และสีแดง คือ **\#3:Small:Red**</span><span class="sxs-lookup"><span data-stu-id="a44eb-146">The name of a product variant that is based on the dimension values Small and Red is **\#3:Small:Red**.</span></span>  

<span data-ttu-id="a44eb-147">ลูกค้าอยากซื้อยืดตัวเล็กสีแดง และชื่อของเสื้อยืดต้องปรากฏเป็นภาษาฝรั่งเศสในใบแจ้งหนี้ </span><span class="sxs-lookup"><span data-stu-id="a44eb-147">A customer wants to buy some small, red T-shirts and the name of the T-shirt must appear in French on the invoice.</span></span> <span data-ttu-id="a44eb-148">คุณแปลค่ามิติ ขนาดเล็กและสีแดง เป็นภาษาฝรั่งเศส และชื่อของผลิตภัณฑ์ย่อยคือ **\#3:Petit:Rouge**</span><span class="sxs-lookup"><span data-stu-id="a44eb-148">You translate the dimension values, Small and Red, into French, and the name of the product variant is **\#3:Petit:Rouge**.</span></span>
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a44eb-149"><strong>คำแนะนำ</strong></span><span class="sxs-lookup"><span data-stu-id="a44eb-149"><strong>Tip</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a44eb-150">การตั้งค่าภาษาที่ต้องการของลูกค้า ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-150">To set the preferred language of a customer, follow these steps:</span></span>
<ol><br/><li><span data-ttu-id="a44eb-151">คลิก <strong>การขายและการตลาด</strong> &gt; <strong>ทั่วไป</strong> &gt; <strong>ลูกค้า</strong> &gt; <strong>ทั้งหมด</strong> <strong>ลูกค้า</strong></span><span class="sxs-lookup"><span data-stu-id="a44eb-151">Click <strong>Sales and marketing</strong> &gt; <strong>Common</strong> &gt; <strong>Customers</strong> &gt; <strong>All</strong> <strong>customers</strong>.</span></span></li>
<li><span data-ttu-id="a44eb-152">ดับเบิลคลิกบัญชีลูกค้าเพื่อเปิดหน้า <strong>ลูกค้า</strong></span><span class="sxs-lookup"><span data-stu-id="a44eb-152">Double-click a customer to open the <strong>Customers</strong> page.</span></span> <span data-ttu-id="a44eb-153">ในแท็บ <strong>ทั่วไป</strong> ในฟิลด์ <strong>ภาษา</strong> เลือก <strong>ภาษา</strong></span><span class="sxs-lookup"><span data-stu-id="a44eb-153">On the <strong>General</strong> tab, in the <strong>Language</strong> field, select the <strong>language</strong>.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a><span data-ttu-id="a44eb-154">จะเกิดอะไรขึ้นหากลูกค้าต้องการใช้ภาษาที่ไม่มีการแปลไว้</span><span class="sxs-lookup"><span data-stu-id="a44eb-154">What happens if a customer has a preferred language for which no translations are available?</span></span>
<span data-ttu-id="a44eb-155">ถ้าไม่มีการแปลอยู่ในภาษาที่ต้องการของลูกค้า ชื่อและคำอธิบายจะปรากฏในภาษาสากลของบริษัทของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="a44eb-155">If translations are not available in the customer’s preferred language, the names and descriptions are displayed in the global language of your own company.</span></span>

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a><span data-ttu-id="a44eb-156">ฉันสามารถจัดการการแปลสำหรับชุดของค่ามิติในเวลาเดียวกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a44eb-156">Can I manage translations for a series of dimension values at the same time?</span></span>
<span data-ttu-id="a44eb-157">ค่ามิติจะเป็นค่าเฉพาะผลิตภัณฑ์ และคุณสามารถจัดการการแปลสำหรับค่ามิติของผลิตภัณฑ์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="a44eb-157">Dimension values are product specific and you can manage the translations for the dimension values for each product.</span></span> <span data-ttu-id="a44eb-158">อย่างไรก็ตาม ถ้าคุณสร้างกลุ่มค่ามิติ และสร้างการแปลสำหรับค่าในกลุ่มค่า จะช่วยให้จัดการการแปลง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="a44eb-158">However, if you create a dimension value group and create translations for the values in the value group, it is easier to manage the translations.</span></span>   

<span data-ttu-id="a44eb-159">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="a44eb-159">**Example**</span></span>  

<span data-ttu-id="a44eb-160">บริษัทของคุณผลิตซื้อเสื้อยืดในลักษณะที่แตกต่างกัน แต่ละลักษณะมีทั้งขนาดเล็ก ขนาดกลาง และขนาดใหญ่</span><span class="sxs-lookup"><span data-stu-id="a44eb-160">Your company produces T-shirts in different styles, and each style is available in the sizes Small, Medium, and Large.</span></span> <span data-ttu-id="a44eb-161">ขนาดต่างๆ ถูกรวบรวมเป็นกลุ่มค่ามิติหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a44eb-161">The sizes are collected in one dimension value group.</span></span> <span data-ttu-id="a44eb-162">เมื่อมีการเพิ่มลักษณะเสื้อยืดใหม่ คุณสามารถเชื่อมโยงกับกลุ่มค่ามิติที่ใช้สำหรับขนาด เพื่อให้ผลิตภัณฑ์ดังกล่าวมีขนาดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="a44eb-162">When a new T-shirt style is added, you can associate it with the dimension value group that is used for sizes, so that all the sizes are available for the product.</span></span> <span data-ttu-id="a44eb-163">นอกจากนี้คุณยังสามารถเพิ่มหรือเปลี่ยนการแปลสำหรับขนาดในกลุ่มค่ามิติได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="a44eb-163">You can also add or change translations for the sizes in the dimension value group at any time.</span></span>  

<span data-ttu-id="a44eb-164">ค่ามิติที่เกี่ยวข้องกับผลิตภัณฑ์โดยใช้กลุ่มตัวแปรมิติ ต้องรักษาจากกลุ่มผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="a44eb-164">A dimension value that is associated with a product through a dimension variant group must be maintained from the product variant group.</span></span>   
<span data-ttu-id="a44eb-165">เมื่อต้องการสร้างกลุ่มค่ามิติ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-165">To create a dimension value group, follow these steps:</span></span>
1.  <span data-ttu-id="a44eb-166">คลิก **การจัดการข้อมูลผลิตภัณฑ์** &gt; **การตั้งค่า** &gt; **กลุ่มตัวแปร**</span><span class="sxs-lookup"><span data-stu-id="a44eb-166">Click **Product information management** &gt; **Setup** &gt; **Variant groups**.</span></span>
2.  <span data-ttu-id="a44eb-167">เลือก **ขนาด** **กลุ่ม** **กลุ่มสี**หรือ **กลุ่มลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-167">Select **Size** **groups**, **Color groups**, or **Style groups**.</span></span>
3.  <span data-ttu-id="a44eb-168">คลิก **สร้าง** แล้วป้อนชื่อสำหรับกลุ่มในฟิลด์ **ขนาด** **กลุ่ม** **กลุ่ม**หรือ **กลุ่มลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-168">Click **New**, and then enter a name for the group in the **Size** **group**, **Color group**, or **Style group** field.</span></span> <span data-ttu-id="a44eb-169">คลิก **ขนาด** **สี**หรือ **ลักษณะ** เพื่อสร้างบรรทัดสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="a44eb-169">Click **Sizes**, **Colors**, or **Styles** to create lines for the groups.</span></span>
4.  <span data-ttu-id="a44eb-170">ในหน้า **ขนาด** **กลุ่ม** บรรทัด **ส** **กลุ่ม** **บรรทัด** หรือ **บรรทัดกลุ่มลักษณะ** คลิก **สร้าง** แล้วสร้างขนาด สี และลักษณะสำหรับกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="a44eb-170">In the **Size** **group** lines, **Color** **group** **lines**, or **Style group lines** page, click **New**, and then create the sizes, colors, and styles for the groups.</span></span>

<span data-ttu-id="a44eb-171">เมื่อต้องการจัดการการแปลสำหรับค่าในกลุ่มค่ามิติ ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="a44eb-171">To manage translations for values in a dimension value group, follow these steps:</span></span>
1.  <span data-ttu-id="a44eb-172">ทำตามขั้นตอนในกระบวนงานก่อนหน้านี้ในการสร้างกลุ่มค่ามิติเพื่อเปิดหน้า **รายการกลุ่มขนาด** **รายการกลุ่มสี**หรือ **รายการกลุ่มลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-172">Follow the steps in the previous procedure for creating a dimension value group to open the **Size group lines**, **Color group lines**, or **Style group lines** page.</span></span>
2.  <span data-ttu-id="a44eb-173">คลิก **การแปลข้อความ**</span><span class="sxs-lookup"><span data-stu-id="a44eb-173">Click **Text translation**.</span></span> <span data-ttu-id="a44eb-174">ในหน้า **การแปลข้อความ** ในกลุ่ม **ข้อความที่แปลแล้ว** ให้ป้อนคำแปลในฟิลด์ **ชื่อ** และ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="a44eb-174">In the **Text translation** page, in the **Translated text** group, enter translations in the **Name** and **Description** fields.</span></span>

## <a name="when-can-translations-of-product-related-information-be-managed"></a><span data-ttu-id="a44eb-175">เมื่อไหร่ที่สามารถจัดการการแปลของข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์ได้</span><span class="sxs-lookup"><span data-stu-id="a44eb-175">When can translations of product-related information be managed?</span></span>
<span data-ttu-id="a44eb-176">สามารถจัดการการแปลของข้อมูลที่เกี่ยวข้องกับผลิตภัณฑ์ได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="a44eb-176">Translations of product-related information can be managed at any time.</span></span> <span data-ttu-id="a44eb-177">เมื่อการแปลได้รับการปรับปรุงสำหรับค่ามิติที่เกี่ยวข้องกับผลิตภัณฑ์ ข้อมูลผลิตภัณฑ์จะได้รับการอัพเดต โดยไม่คำนึงถึงว่าผลิตภัณฑ์มีธุรกรรมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="a44eb-177">When translations are updated for a dimension value that is associated with a product, the product information is updated, regardless of whether the product has transactions.</span></span>






