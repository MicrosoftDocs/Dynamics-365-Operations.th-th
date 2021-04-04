---
title: โมดูลการแชร์ทางสังคม
description: หัวข้อนี้ครอบคลุมถึงโมดูลการแชร์ทางสังคมและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234328"
---
# <a name="social-share-module"></a><span data-ttu-id="e7df3-103">โมดูลการแชร์ในสังคมออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e7df3-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7df3-104">หัวข้อนี้ครอบคลุมถึงโมดูลการแชร์ทางสังคมและอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e7df3-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e7df3-105">โมดูลการแชร์ทางสังคมอนุญาตให้ผู้ใช้สามารถแชร์ URL ของเว็บไซต์อีคอมเมิร์ซบนสื่อสังคม เช่น Facebook, Twitter, Pinterest และ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="e7df3-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="e7df3-106">นอกจากนี้ คุณยังสามารถแชร์ URL ของหน้าไซต์ผ่านทางอีเมลได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="e7df3-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="e7df3-107">โมดูลการแชร์ทางสังคมใช้โดยทั่วไปบนหน้ารายละเอียดผลิตภัณฑ์ (PDP) เพื่อช่วยให้ผู้ใช้สามารถแชร์ข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7df3-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="e7df3-108">โมดูลการแชร์ทางสังคมแต่ละโมดูลคือคอนเทนเนอร์สำหรับโมดูลสินค้าที่มีการแชร์ทางสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="e7df3-109">โมดูลสินค้าที่มีการแชร์ทางสังคมแต่ละโมดูลสามารถตั้งค่าคอนฟิกให้ชี้ไปที่ไซต์สื่อสังคมเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e7df3-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="e7df3-110">การรวมกับ Facebook, Twitter, Pinterest, LinkedIn และอีเมลจะได้รับการสนับสนุนให้ใช้ได้ทันที</span><span class="sxs-lookup"><span data-stu-id="e7df3-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="e7df3-111">เมื่อผู้ใช้ไซต์เลือกสัญลักษณ์สื่อสังคม จะมีการเปิดใช้งาน iframe ของ HTML สำหรับไซต์สื่อสังคมที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e7df3-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="e7df3-112">ภายใน iframe ผู้ใช้สามารถลงชื่อเข้าใช้และโพสต์เนื้อหาของหน้าที่พวกเขาดูได้</span><span class="sxs-lookup"><span data-stu-id="e7df3-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="e7df3-113">แพลตฟอร์มสื่อสังคมแต่ละแพลตฟอร์มอาจติดตามคุกกี้ ดังนั้นโมดูลนี้ต้องการให้ผู้ใช้ไซต์ยอมรับข้อความการแจ้งเตือนเกี่ยวกับการยินยอมใช้คุกกี้</span><span class="sxs-lookup"><span data-stu-id="e7df3-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="e7df3-114">เมื่อไม่มีการยอมรับการยินยอมใช้คุ้กกี้ โมดูลนี้จะถูกซ่อนบนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e7df3-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="e7df3-115">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การปฏิบัติตามข้อกำหนดคุกกี้](cookie-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="e7df3-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="e7df3-116">ภาพประกอบต่อไปนี้เน้นตัวอย่างของโมดูลการแชร์ทางสังคมซึ่งใช้ในหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7df3-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![ตัวอย่างของโมดูลการแชร์ทางสังคม](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="e7df3-118">คุณสมบัติของโมดูลการแชร์ทางสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-118">Social share module properties</span></span>

| <span data-ttu-id="e7df3-119">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="e7df3-119">Property name</span></span>             | <span data-ttu-id="e7df3-120">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="e7df3-120">Value</span></span>                 | <span data-ttu-id="e7df3-121">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e7df3-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e7df3-122">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e7df3-122">Caption</span></span>                  | <span data-ttu-id="e7df3-123">ข้อความ</span><span class="sxs-lookup"><span data-stu-id="e7df3-123">Text</span></span> | <span data-ttu-id="e7df3-124">คุณสมบัตินี้จะระบุคำอธิบายสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="e7df3-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="e7df3-125">การวางแนว</span><span class="sxs-lookup"><span data-stu-id="e7df3-125">Orientation</span></span> | <span data-ttu-id="e7df3-126">**แนวนอน** หรือ **แนวตั้ง**</span><span class="sxs-lookup"><span data-stu-id="e7df3-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="e7df3-127">คุณสมบัตินี้จะกำหนดแนวโครงร่างสำหรับสินค้าบนสื่อสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="e7df3-128">คุณสมบัติของโมดูลสินค้าที่มีการแชร์ทางสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-128">Social share item module properties</span></span>
| <span data-ttu-id="e7df3-129">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="e7df3-129">Property name</span></span>             | <span data-ttu-id="e7df3-130">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="e7df3-130">Value</span></span>                 | <span data-ttu-id="e7df3-131">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e7df3-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e7df3-132">สื่อสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-132">Social media</span></span>              | <span data-ttu-id="e7df3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **จดหมาย**</span><span class="sxs-lookup"><span data-stu-id="e7df3-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="e7df3-134">เมนูแบบหล่นลงที่มีรายชื่อของแพลตฟอร์มสื่อสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="e7df3-135">ไอคอน</span><span class="sxs-lookup"><span data-stu-id="e7df3-135">Icon</span></span> |<span data-ttu-id="e7df3-136">รูป</span><span class="sxs-lookup"><span data-stu-id="e7df3-136">Image</span></span>    | <span data-ttu-id="e7df3-137">รายการนี้จะเป็นรูปภาพที่จะแสดงให้เห็นในสื่อสังคมที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e7df3-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="e7df3-138">ในฐานะแนวทางปฏิบัติที่ดีที่สุดด ให้อ้างอิง SDK ของแพลตฟอร์มสื่อสังคมสำหรับรูปภาพที่แนะนำในการใช้งานสำหรับแต่ละแพลตฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="e7df3-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="e7df3-139">เพิ่มโมดูลการแชร์ทางสังคมในโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7df3-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="e7df3-140">หากต้องการเพิ่มโมดูลการแชร์ทางสังคมในโมดูลกล่องการซื้อ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e7df3-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="e7df3-141">ในไซต์ Fabrikam เลือก **หน้า** แล้วเลือกหน้า **DefaultPDP** เพื่อเปิดหน้ารายละเอียดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="e7df3-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="e7df3-142">ในช่อง **กล่องการซื้อ (จำเป็น)** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="e7df3-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7df3-143">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การแชร์ทางสังคม** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7df3-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7df3-144">ในช่อง **การแชร์ทางสังคม** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="e7df3-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7df3-145">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การแชร์ทางสังคม** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7df3-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7df3-146">ในบานหน้าต่างคุณสมบัติของโมดูล **การแชร์ทางสังคม** ภายใต้ **การจัดแนว** ให้เลือก **แนวนอน**</span><span class="sxs-lookup"><span data-stu-id="e7df3-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="e7df3-147">เพิ่มคำอธิบายเฉพาะเมื่อจำเป็น</span><span class="sxs-lookup"><span data-stu-id="e7df3-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="e7df3-148">ในช่อง **การแชร์ทางสังคม** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="e7df3-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7df3-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **SocialShareItem** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7df3-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e7df3-150">ในบานหน้าต่างคุณสมบัติของโมดูล **SocialShareItem** ภายใต้ **สื่อสังคม** เลือก **Facebook**</span><span class="sxs-lookup"><span data-stu-id="e7df3-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="e7df3-151">ในบานหน้าต่างคุณสมบัติของโมดูล **SocialShareItem** ภายใต้ **ไอคอน** เลือก **+ เพิ่มรูปภาพ**</span><span class="sxs-lookup"><span data-stu-id="e7df3-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="e7df3-152">ในกล่องโต้ตอบ **ตัวเลือกสื่อ** ให้เลือกรูปภาพโลโก้ Facebook แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e7df3-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="e7df3-153">ถ้าไม่มีรูปภาพโลโก้ Facebook ให้เลือก **อัปโหลดรายการสื่อใหม่** เพื่ออัปโหลด</span><span class="sxs-lookup"><span data-stu-id="e7df3-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="e7df3-154">เพิ่มและตั้งค่าคอนฟิกโมดูล **SocialShareItem** เพิ่มเติมได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="e7df3-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="e7df3-155">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="e7df3-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e7df3-156">หน้าดังกล่าวจะแสดงโมดูลการแชร์ทางสังคม</span><span class="sxs-lookup"><span data-stu-id="e7df3-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="e7df3-157">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="e7df3-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7df3-158">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e7df3-158">Additional resources</span></span>

[<span data-ttu-id="e7df3-159">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="e7df3-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e7df3-160">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="e7df3-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e7df3-161">การคาดการณ์ความต้องการคุกกี้</span><span class="sxs-lookup"><span data-stu-id="e7df3-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]