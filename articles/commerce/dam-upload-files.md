---
title: อัพโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ
description: หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์ไบนารีนอกเหนือจากภาพและวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799264"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="494c9-103">อัปโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="494c9-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="494c9-104">หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์นอกเหนือจากภาพและวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="494c9-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="494c9-105">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce สนับสนุนการอัพโหลดสินทรัพย์ไบนารี นอกเหนือจากรูปภาพหรือวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="494c9-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="494c9-106">ตัวอย่างเช่น คุณอาจต้องการอัพโหลด Microsoft Excel Microsoft Word Microsoft PowerPoint หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="494c9-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="494c9-107">ชนิดเอกสารต่อไปนี้ได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="494c9-107">The following document types are supported:</span></span>
- <span data-ttu-id="494c9-108">7Z</span><span class="sxs-lookup"><span data-stu-id="494c9-108">7Z</span></span>
- <span data-ttu-id="494c9-109">AVI</span><span class="sxs-lookup"><span data-stu-id="494c9-109">AVI</span></span>
- <span data-ttu-id="494c9-110">CS</span><span class="sxs-lookup"><span data-stu-id="494c9-110">CS</span></span>
- <span data-ttu-id="494c9-111">CSS</span><span class="sxs-lookup"><span data-stu-id="494c9-111">CSS</span></span>
- <span data-ttu-id="494c9-112">DOC</span><span class="sxs-lookup"><span data-stu-id="494c9-112">DOC</span></span>
- <span data-ttu-id="494c9-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="494c9-113">DOCX</span></span>
- <span data-ttu-id="494c9-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="494c9-114">EPUB</span></span>
- <span data-ttu-id="494c9-115">GIF</span><span class="sxs-lookup"><span data-stu-id="494c9-115">GIF</span></span>
- <span data-ttu-id="494c9-116">INDD</span><span class="sxs-lookup"><span data-stu-id="494c9-116">INDD</span></span>
- <span data-ttu-id="494c9-117">JAR</span><span class="sxs-lookup"><span data-stu-id="494c9-117">JAR</span></span>
- <span data-ttu-id="494c9-118">JPG</span><span class="sxs-lookup"><span data-stu-id="494c9-118">JPG</span></span>
- <span data-ttu-id="494c9-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="494c9-119">JPEG</span></span>
- <span data-ttu-id="494c9-120">JS</span><span class="sxs-lookup"><span data-stu-id="494c9-120">JS</span></span>
- <span data-ttu-id="494c9-121">MP3</span><span class="sxs-lookup"><span data-stu-id="494c9-121">MP3</span></span>
- <span data-ttu-id="494c9-122">MP4</span><span class="sxs-lookup"><span data-stu-id="494c9-122">MP4</span></span>
- <span data-ttu-id="494c9-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="494c9-123">MPEG</span></span>
- <span data-ttu-id="494c9-124">MPG</span><span class="sxs-lookup"><span data-stu-id="494c9-124">MPG</span></span>
- <span data-ttu-id="494c9-125">ODP</span><span class="sxs-lookup"><span data-stu-id="494c9-125">ODP</span></span>
- <span data-ttu-id="494c9-126">ODS</span><span class="sxs-lookup"><span data-stu-id="494c9-126">ODS</span></span>
- <span data-ttu-id="494c9-127">ODT</span><span class="sxs-lookup"><span data-stu-id="494c9-127">ODT</span></span>
- <span data-ttu-id="494c9-128">PDF</span><span class="sxs-lookup"><span data-stu-id="494c9-128">PDF</span></span>
- <span data-ttu-id="494c9-129">PNG</span><span class="sxs-lookup"><span data-stu-id="494c9-129">PNG</span></span>
- <span data-ttu-id="494c9-130">PPT</span><span class="sxs-lookup"><span data-stu-id="494c9-130">PPT</span></span>
- <span data-ttu-id="494c9-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="494c9-131">PPTX</span></span>
- <span data-ttu-id="494c9-132">PS</span><span class="sxs-lookup"><span data-stu-id="494c9-132">PS</span></span>
- <span data-ttu-id="494c9-133">QXP</span><span class="sxs-lookup"><span data-stu-id="494c9-133">QXP</span></span>
- <span data-ttu-id="494c9-134">RAR</span><span class="sxs-lookup"><span data-stu-id="494c9-134">RAR</span></span>
- <span data-ttu-id="494c9-135">RTF</span><span class="sxs-lookup"><span data-stu-id="494c9-135">RTF</span></span>
- <span data-ttu-id="494c9-136">SVG</span><span class="sxs-lookup"><span data-stu-id="494c9-136">SVG</span></span>
- <span data-ttu-id="494c9-137">TAR</span><span class="sxs-lookup"><span data-stu-id="494c9-137">TAR</span></span>
- <span data-ttu-id="494c9-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="494c9-138">TGZ</span></span>
- <span data-ttu-id="494c9-139">TXT</span><span class="sxs-lookup"><span data-stu-id="494c9-139">TXT</span></span>
- <span data-ttu-id="494c9-140">WMV</span><span class="sxs-lookup"><span data-stu-id="494c9-140">WMV</span></span>
- <span data-ttu-id="494c9-141">XLS</span><span class="sxs-lookup"><span data-stu-id="494c9-141">XLS</span></span>
- <span data-ttu-id="494c9-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="494c9-142">XLSX</span></span>
- <span data-ttu-id="494c9-143">XML</span><span class="sxs-lookup"><span data-stu-id="494c9-143">XML</span></span>
- <span data-ttu-id="494c9-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="494c9-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="494c9-145">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="494c9-145">Upload a file</span></span>

<span data-ttu-id="494c9-146">หากต้องการอัพโหลดไฟล์ไปยังโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="494c9-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="494c9-147">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="494c9-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="494c9-148">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="494c9-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="494c9-149">ในตัวสำรวจไฟล์ ให้เลือกไฟล์ตั้งแต่หนึ่งไฟล์ขึ้นไป แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="494c9-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="494c9-150">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่อง คำอธิบาย และข้อมูลเมตาของคำสำคัญ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="494c9-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="494c9-151">เมื่อต้องการเผยแพร่ไฟล์หลังจากการอัพโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากการอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="494c9-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="494c9-152">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="494c9-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="494c9-153">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="494c9-153">Additional resources</span></span>

[<span data-ttu-id="494c9-154">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="494c9-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="494c9-155">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="494c9-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="494c9-156">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="494c9-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="494c9-157">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="494c9-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="494c9-158">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="494c9-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="494c9-159">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="494c9-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
