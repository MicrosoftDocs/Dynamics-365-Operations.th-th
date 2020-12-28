---
title: อัพโหลดวิดีโอ
description: หัวข้อนี้อธิบายวิธีการอัพโหลดวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8dd9e710f9a6ea593a0673e7902fadf84ca05cff
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594319"
---
# <a name="upload-videos"></a><span data-ttu-id="1c9a4-103">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c9a4-104">หัวข้อนี้อธิบายวิธีการอัพโหลดวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1c9a4-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="1c9a4-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="1c9a4-105">Overview</span></span>

<span data-ttu-id="1c9a4-106">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce ช่วยให้คุณสามารถอัพโหลดวิดีโอได้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="1c9a4-107">คุณควรอัพโหลดรุ่นของวิดีโอที่มีบิตเรตและความละเอียดสูงสุดเสมอ เนื่องจากวิดีโอจะถูกแปลงโดยอัตโนมัติเพื่อให้เหมาะสมกับ viewports และจุดสั่งหยุดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="1c9a4-108">ข้อมูลวิดีโอที่ระบุระหว่างการอัพโหลด</span><span class="sxs-lookup"><span data-stu-id="1c9a4-108">Video information specified during upload</span></span>

<span data-ttu-id="1c9a4-109">เมื่ออัพโหลดวิดีโอ คุณสามารถระบุข้อมูลต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="1c9a4-110">**ชื่อเรื่อง คำอธิบาย คำสำคัญ**: ข้อมูลเมตาของวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="1c9a4-111">**สร้างคำอธิบายที่ปิดโดยอัตโนมัติ**: ระบุว่าควรจะสร้างคำอธิบายที่ปิดสำหรับวิดีโอโดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1c9a4-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="1c9a4-112">**คำอธิบายที่ปิด**: ระบุคำอธิบายที่ปิดที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="1c9a4-113">**เสียงปกติ**: ระบุแทร็กเสียงทั่วไปที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="1c9a4-114">**รูปขนาดย่อ**: ระบุรูปขนาดย่อสำหรับวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="1c9a4-115">ถ้าไม่ได้ระบุ จะมีการสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="1c9a4-116">**เสียงอธิบาย**: ระบุแทร็กเสียงอธิบายที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="1c9a4-117">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-117">Upload a video</span></span>

<span data-ttu-id="1c9a4-118">เมื่อต้องการอัพโหลดวิดีโอในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1c9a4-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="1c9a4-119">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="1c9a4-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="1c9a4-120">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="1c9a4-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="1c9a4-121">ในหน้าต่างตัวสำรวจไฟล์ ให้นำทางไปยังและเลือกไฟล์วิดีโอหนึ่งไฟล์ขึ้นไปที่จะอัพโหลด แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="1c9a4-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="1c9a4-122">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่องและข้อความกำกับที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="1c9a4-123">ป้อนคำอธิบายและคำสำคัญที่เลือกกำหนดได้ และเลือกประเภทถ้าต้องการ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="1c9a4-124">ถ้าคุณต้องการเผยแพร่รูปภาพหลังจากอัปโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="1c9a4-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="1c9a4-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c9a4-125">Select **OK**.</span></span>

<span data-ttu-id="1c9a4-126">ถ้าคุณกำลังอัพโหลดสินทรัพย์หลายชนิดพร้อมกัน (ตัวอย่างเช่น รูปภาพและวิดีโอ) ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** คุณจะสามารถระบุคำสำคัญได้ทันทีว่าควรเผยแพร่ไฟล์ในทันทีหลังจากอัพโหลดหรือไม่ และควรสร้างคำอธิบายที่ปิดสำหรับไฟล์วิดีโอโดยอัตโนมัติหรือไม่</span><span class="sxs-lookup"><span data-stu-id="1c9a4-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="1c9a4-127">สินทรัพย์ทั้งหมดจะมีการใช้คำสำคัญเดียวกันร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="1c9a4-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c9a4-128">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1c9a4-128">Additional resources</span></span>

[<span data-ttu-id="1c9a4-129">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="1c9a4-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="1c9a4-130">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="1c9a4-131">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="1c9a4-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="1c9a4-132">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="1c9a4-133">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="1c9a4-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="1c9a4-134">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="1c9a4-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
