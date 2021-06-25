---
title: อัพโหลดวิดีโอ
description: หัวข้อนี้อธิบายวิธีการอัปโหลดวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 06/09/2021
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
ms.openlocfilehash: e3579b54c58898b79c84406480a3b58f541c4621
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224549"
---
# <a name="upload-videos"></a><span data-ttu-id="86062-103">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="86062-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86062-104">หัวข้อนี้อธิบายวิธีการอัปโหลดวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="86062-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="86062-105">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce ช่วยให้คุณสามารถอัพโหลดวิดีโอได้</span><span class="sxs-lookup"><span data-stu-id="86062-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="86062-106">คุณควรอัพโหลดรุ่นของวิดีโอที่มีบิตเรตและความละเอียดสูงสุดเสมอ เนื่องจากวิดีโอจะถูกแปลงโดยอัตโนมัติเพื่อให้เหมาะสมกับ viewports และจุดสั่งหยุดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="86062-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="86062-107">ข้อมูลวิดีโอที่ระบุระหว่างการอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="86062-107">Video information specified during upload</span></span>

<span data-ttu-id="86062-108">เมื่ออัพโหลดวิดีโอ คุณสามารถระบุข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="86062-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="86062-109">**ชื่อเรื่อง คำอธิบาย คำสำคัญ**: ข้อมูลเมตาของวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="86062-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="86062-110">**สร้างคำอธิบายที่ปิดโดยอัตโนมัติ**: ระบุว่าควรจะสร้างคำอธิบายที่ปิดสำหรับวิดีโอโดยอัตโนมัติหรือไม่ (สนับสนุนภาษาอังกฤษเท่านั้น)</span><span class="sxs-lookup"><span data-stu-id="86062-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video (only English language is supported).</span></span> 
- <span data-ttu-id="86062-111">**คำอธิบายที่ปิด**: ระบุคำอธิบายที่ปิดที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="86062-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="86062-112">**เสียงปกติ**: ระบุแทร็กเสียงทั่วไปที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="86062-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="86062-113">**รูปขนาดย่อ**: ระบุรูปขนาดย่อสำหรับวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="86062-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="86062-114">ถ้าไม่ได้ระบุ จะมีการสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="86062-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="86062-115">**เสียงอธิบาย**: ระบุแทร็กเสียงอธิบายที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="86062-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="86062-116">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="86062-116">Upload a video</span></span>

<span data-ttu-id="86062-117">เมื่อต้องการอัพโหลดวิดีโอในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="86062-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="86062-118">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="86062-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="86062-119">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="86062-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="86062-120">ในหน้าต่างตัวสำรวจไฟล์ ให้นำทางไปยังและเลือกไฟล์วิดีโอหนึ่งไฟล์ขึ้นไปที่จะอัพโหลด แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="86062-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="86062-121">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่องและข้อความกำกับที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="86062-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="86062-122">ป้อนคำอธิบายและคำสำคัญที่เลือกกำหนดได้ และเลือกประเภทถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="86062-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="86062-123">ถ้าคุณต้องการเผยแพร่รูปภาพหลังจากอัปโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="86062-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="86062-124">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="86062-124">Select **OK**.</span></span>

<span data-ttu-id="86062-125">ถ้าคุณกำลังอัพโหลดสินทรัพย์หลายชนิดพร้อมกัน (ตัวอย่างเช่น รูปภาพและวิดีโอ) ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** คุณจะสามารถระบุคำสำคัญได้ทันทีว่าควรเผยแพร่ไฟล์ในทันทีหลังจากอัพโหลดหรือไม่ และควรสร้างคำอธิบายที่ปิดสำหรับไฟล์วิดีโอโดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="86062-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="86062-126">สินทรัพย์ทั้งหมดจะมีการใช้คำสำคัญเดียวกันร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="86062-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86062-127">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="86062-127">Additional resources</span></span>

[<span data-ttu-id="86062-128">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="86062-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="86062-129">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="86062-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="86062-130">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="86062-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="86062-131">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="86062-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="86062-132">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="86062-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="86062-133">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="86062-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
