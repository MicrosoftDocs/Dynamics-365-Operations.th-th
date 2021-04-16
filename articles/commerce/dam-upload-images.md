---
title: อัพโหลดรูปภาพ
description: หัวข้อนี้อธิบายวิธีการอัปโหลดภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799240"
---
# <a name="upload-images"></a><span data-ttu-id="93ca0-103">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="93ca0-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93ca0-104">หัวข้อนี้อธิบายวิธีการอัปโหลดภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="93ca0-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="93ca0-105">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce ช่วยให้คุณสามารถอัพโหลดรูปภาพโดยลำพัง หรือเป็นกลุ่ม โดยใช้โฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="93ca0-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="93ca0-106">คุณควรอัพโหลดรุ่นของรูปภาพที่มีความละเอียดและคุณภาพสูงสุดเสมอ เนื่องจากส่วนประกอบของตัวปรับขนาดรูปภาพจะปรับรูปภาพให้เหมาะสมโดยอัตโนมัติสำหรับ viewports และจุดสั่งหยุดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="93ca0-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="93ca0-107">ข้อมูลรูปภาพที่ระบุระหว่างการอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="93ca0-107">Image information specified during upload</span></span>

<span data-ttu-id="93ca0-108">เมื่ออัพโหลดรูปภาพ คุณสามารถระบุข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="93ca0-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="93ca0-109">**ชื่อเรื่อง ข้อความกำกับ คำอธิบาย คำสำคัญ**: ข้อมูลเมตาของรูปภาพหนึ่งหรือรูปภาพต่างๆ</span><span class="sxs-lookup"><span data-stu-id="93ca0-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="93ca0-110">ชื่อเรื่องและข้อความกำกับเป็นค่าที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="93ca0-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="93ca0-111">**เลือกประเภท**:</span><span class="sxs-lookup"><span data-stu-id="93ca0-111">**Select category**:</span></span>
    - <span data-ttu-id="93ca0-112">**ไม่มี**: ถูกใช้สำหรับรูปภาพหนึ่งหรือรูปภาพต่างๆ ในการเล่าเรื่องของอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="93ca0-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="93ca0-113">**ผลิตภัณฑ์ ประเภท ลูกค้า พนักงาน แค็ตตาล็อก**: ถูกใช้สำหรับรูปภาพหนึ่งหรือรูปภาพต่างๆ ของช่องทาง omni ของ Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="93ca0-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="93ca0-114">**เผยแพร่สินทรัพย์หลังจากการอัพโหลด**: เมื่อเลือกกล่องกาเครื่องหมายนี้ จะมีการเผยแพร่รูปภาพหนึ่งหรือรูปภาพต่างๆ โดยทันทีหลังจากการอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="93ca0-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="93ca0-115">นอกจากนี้ สินทรัพย์ของรูปภาพที่มีประเภทที่กำหนดไว้จะถูกติดป้ายโดยอัตโนมัติโดยมีประเภทเป็นคำสำคัญที่จะช่วยในการค้นหาสินทรัพย์ของประเภทที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="93ca0-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="93ca0-116">แบบแผนการตั้งชื่อสำหรับรูปแบบช่องทาง omni</span><span class="sxs-lookup"><span data-stu-id="93ca0-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="93ca0-117">ถ้าคุณได้ตั้งค่าคอนฟิกไลบรารีสื่อเป็นแบ็กเอนด์ของช่องทาง omni คุณสามารถใช้ประเภทของรูปภาพเพื่อระบุประเภทที่รูปภาพที่อัพโหลดอยู่</span><span class="sxs-lookup"><span data-stu-id="93ca0-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="93ca0-118">นอกจากนี้ ยังมีแบบแผนการตั้งชื่อที่ควรถูกติดตาม เพื่อให้แน่ใจว่ามีการดึงข้อมูลรูปภาพอย่างถูกต้องโดยช่องทางอื่นๆ เช่น การขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="93ca0-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="93ca0-119">แบบแผนการตั้งชื่อเริ่มต้นจะแตกต่างกันไปตามประเภท:</span><span class="sxs-lookup"><span data-stu-id="93ca0-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="93ca0-120">รูปภาพในแค็ตตาล็อกควรมีชื่อว่า "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="93ca0-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="93ca0-121">รูปภาพของประเภทควรมีชื่อว่า "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="93ca0-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="93ca0-122">รูปภาพของลูกค้าควรมีชื่อว่า "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="93ca0-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="93ca0-123">รูปภาพพนักงานควรมีชื่อว่า "**/Workers/\{WorkerNumber\}.jpg**</span><span class="sxs-lookup"><span data-stu-id="93ca0-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="93ca0-124">รูปภาพของผลิตภัณฑ์ควรมีชื่อว่า "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="93ca0-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="93ca0-125">001 เป็นลำดับของรูปภาพ และอาจเป็น 001 002 003 004 หรือ 005</span><span class="sxs-lookup"><span data-stu-id="93ca0-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="93ca0-126">รูปภาพของผลิตภัณฑ์ย่อยควรมีชื่อว่า "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="93ca0-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="93ca0-127">ตัวอย่างเช่น: 93039 \^ \^ 2 \^ Black \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="93ca0-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="93ca0-128">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="93ca0-128">Upload an image</span></span>

<span data-ttu-id="93ca0-129">เมื่อต้องการอัพโหลดรูปภาพในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="93ca0-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="93ca0-130">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="93ca0-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="93ca0-131">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="93ca0-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="93ca0-132">ในหน้าต่างตัวสำรวจไฟล์ ให้นำทางไปและเลือกไฟล์รูปภาพหนึ่งไฟล์ขึ้นไปที่จะอัพโหลด แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="93ca0-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="93ca0-133">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่องและข้อความกำกับที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="93ca0-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="93ca0-134">ป้อนคำอธิบายและคำสำคัญที่เลือกกำหนดได้ และเลือกประเภทถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="93ca0-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="93ca0-135">ถ้าคุณต้องการเผยแพร่รูปภาพหลังจากการอัพโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากการอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="93ca0-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="93ca0-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="93ca0-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="93ca0-137">อัพโหลดโฟลเดอร์ของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="93ca0-137">Upload a folder of images</span></span>

<span data-ttu-id="93ca0-138">เมื่อต้องการอัพโหลดโฟลเดอร์ของรูปภาพจำนวนมากในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="93ca0-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="93ca0-139">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="93ca0-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="93ca0-140">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดโฟลเดอร์**</span><span class="sxs-lookup"><span data-stu-id="93ca0-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="93ca0-141">ในหน้าต่างตัวสำรวจไฟล์ ให้นำทางไปและเลือกโฟลเดอร์เพื่ออัพโหลด แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="93ca0-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="93ca0-142">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนคำสำคัญที่ไม่จำเป็น และเลือกประเภทถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="93ca0-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="93ca0-143">ถ้าคุณต้องการเผยแพร่รูปภาพในโฟลเดอร์โดยทันทีหลังจากการอัพโหลด ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากการอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="93ca0-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="93ca0-144">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="93ca0-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93ca0-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="93ca0-145">Additional resources</span></span>

[<span data-ttu-id="93ca0-146">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="93ca0-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="93ca0-147">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="93ca0-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="93ca0-148">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="93ca0-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="93ca0-149">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="93ca0-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="93ca0-150">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="93ca0-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="93ca0-151">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="93ca0-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
