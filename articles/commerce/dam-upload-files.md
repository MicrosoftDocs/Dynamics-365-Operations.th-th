---
title: อัพโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ
description: หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์ไบนารี นอกเหนือจากรูปภาพและวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995781"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="33f04-103">อัพโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="33f04-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33f04-104">หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์ นอกเหนือจากรูปภาพและวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="33f04-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="33f04-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="33f04-105">Overview</span></span>

<span data-ttu-id="33f04-106">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce สนับสนุนการอัพโหลดสินทรัพย์ไบนารี นอกเหนือจากรูปภาพหรือวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="33f04-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="33f04-107">ตัวอย่างเช่น คุณอาจต้องการอัพโหลด Microsoft Excel Microsoft Word Microsoft PowerPoint หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="33f04-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="33f04-108">ชนิดเอกสารต่อไปนี้ได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="33f04-108">The following document types are supported:</span></span>
- <span data-ttu-id="33f04-109">7Z</span><span class="sxs-lookup"><span data-stu-id="33f04-109">7Z</span></span>
- <span data-ttu-id="33f04-110">AVI</span><span class="sxs-lookup"><span data-stu-id="33f04-110">AVI</span></span>
- <span data-ttu-id="33f04-111">CS</span><span class="sxs-lookup"><span data-stu-id="33f04-111">CS</span></span>
- <span data-ttu-id="33f04-112">CSS</span><span class="sxs-lookup"><span data-stu-id="33f04-112">CSS</span></span>
- <span data-ttu-id="33f04-113">DOC</span><span class="sxs-lookup"><span data-stu-id="33f04-113">DOC</span></span>
- <span data-ttu-id="33f04-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="33f04-114">DOCX</span></span>
- <span data-ttu-id="33f04-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="33f04-115">EPUB</span></span>
- <span data-ttu-id="33f04-116">GIF</span><span class="sxs-lookup"><span data-stu-id="33f04-116">GIF</span></span>
- <span data-ttu-id="33f04-117">INDD</span><span class="sxs-lookup"><span data-stu-id="33f04-117">INDD</span></span>
- <span data-ttu-id="33f04-118">JAR</span><span class="sxs-lookup"><span data-stu-id="33f04-118">JAR</span></span>
- <span data-ttu-id="33f04-119">JPG</span><span class="sxs-lookup"><span data-stu-id="33f04-119">JPG</span></span>
- <span data-ttu-id="33f04-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="33f04-120">JPEG</span></span>
- <span data-ttu-id="33f04-121">JS</span><span class="sxs-lookup"><span data-stu-id="33f04-121">JS</span></span>
- <span data-ttu-id="33f04-122">MP3</span><span class="sxs-lookup"><span data-stu-id="33f04-122">MP3</span></span>
- <span data-ttu-id="33f04-123">MP4</span><span class="sxs-lookup"><span data-stu-id="33f04-123">MP4</span></span>
- <span data-ttu-id="33f04-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="33f04-124">MPEG</span></span>
- <span data-ttu-id="33f04-125">MPG</span><span class="sxs-lookup"><span data-stu-id="33f04-125">MPG</span></span>
- <span data-ttu-id="33f04-126">ODP</span><span class="sxs-lookup"><span data-stu-id="33f04-126">ODP</span></span>
- <span data-ttu-id="33f04-127">ODS</span><span class="sxs-lookup"><span data-stu-id="33f04-127">ODS</span></span>
- <span data-ttu-id="33f04-128">ODT</span><span class="sxs-lookup"><span data-stu-id="33f04-128">ODT</span></span>
- <span data-ttu-id="33f04-129">PDF</span><span class="sxs-lookup"><span data-stu-id="33f04-129">PDF</span></span>
- <span data-ttu-id="33f04-130">PNG</span><span class="sxs-lookup"><span data-stu-id="33f04-130">PNG</span></span>
- <span data-ttu-id="33f04-131">PPT</span><span class="sxs-lookup"><span data-stu-id="33f04-131">PPT</span></span>
- <span data-ttu-id="33f04-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="33f04-132">PPTX</span></span>
- <span data-ttu-id="33f04-133">PS</span><span class="sxs-lookup"><span data-stu-id="33f04-133">PS</span></span>
- <span data-ttu-id="33f04-134">QXP</span><span class="sxs-lookup"><span data-stu-id="33f04-134">QXP</span></span>
- <span data-ttu-id="33f04-135">RAR</span><span class="sxs-lookup"><span data-stu-id="33f04-135">RAR</span></span>
- <span data-ttu-id="33f04-136">RTF</span><span class="sxs-lookup"><span data-stu-id="33f04-136">RTF</span></span>
- <span data-ttu-id="33f04-137">SVG</span><span class="sxs-lookup"><span data-stu-id="33f04-137">SVG</span></span>
- <span data-ttu-id="33f04-138">TAR</span><span class="sxs-lookup"><span data-stu-id="33f04-138">TAR</span></span>
- <span data-ttu-id="33f04-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="33f04-139">TGZ</span></span>
- <span data-ttu-id="33f04-140">TXT</span><span class="sxs-lookup"><span data-stu-id="33f04-140">TXT</span></span>
- <span data-ttu-id="33f04-141">WMV</span><span class="sxs-lookup"><span data-stu-id="33f04-141">WMV</span></span>
- <span data-ttu-id="33f04-142">XLS</span><span class="sxs-lookup"><span data-stu-id="33f04-142">XLS</span></span>
- <span data-ttu-id="33f04-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="33f04-143">XLSX</span></span>
- <span data-ttu-id="33f04-144">XML</span><span class="sxs-lookup"><span data-stu-id="33f04-144">XML</span></span>
- <span data-ttu-id="33f04-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="33f04-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="33f04-146">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="33f04-146">Upload a file</span></span>

<span data-ttu-id="33f04-147">หากต้องการอัพโหลดไฟล์ไปยังโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="33f04-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="33f04-148">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="33f04-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="33f04-149">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="33f04-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="33f04-150">ในตัวสำรวจไฟล์ ให้เลือกไฟล์ตั้งแต่หนึ่งไฟล์ขึ้นไป แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="33f04-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="33f04-151">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่อง คำอธิบาย และข้อมูลเมตาของคำสำคัญ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="33f04-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="33f04-152">เมื่อต้องการเผยแพร่ไฟล์หลังจากการอัพโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากการอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="33f04-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="33f04-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="33f04-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33f04-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="33f04-154">Additional resources</span></span>

[<span data-ttu-id="33f04-155">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="33f04-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="33f04-156">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="33f04-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="33f04-157">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="33f04-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="33f04-158">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="33f04-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="33f04-159">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="33f04-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="33f04-160">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="33f04-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
