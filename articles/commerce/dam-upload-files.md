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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097090"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="5de9e-103">อัพโหลดไฟล์นอกเหนือจากรูปภาพและวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="5de9e-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5de9e-104">หัวข้อนี้จะอธิบายวิธีการอัพโหลดไฟล์ นอกเหนือจากรูปภาพและวิดีโอในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5de9e-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="5de9e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5de9e-105">Overview</span></span>

<span data-ttu-id="5de9e-106">ไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce สนับสนุนการอัพโหลดสินทรัพย์ไบนารี นอกเหนือจากรูปภาพหรือวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="5de9e-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="5de9e-107">ตัวอย่างเช่น คุณอาจต้องการอัพโหลด Microsoft Excel Microsoft Word Microsoft PowerPoint หรือไฟล์ PDF</span><span class="sxs-lookup"><span data-stu-id="5de9e-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="5de9e-108">ชนิดเอกสารต่อไปนี้ได้รับการสนับสนุน:</span><span class="sxs-lookup"><span data-stu-id="5de9e-108">The following document types are supported:</span></span>
- <span data-ttu-id="5de9e-109">7Z</span><span class="sxs-lookup"><span data-stu-id="5de9e-109">7Z</span></span>
- <span data-ttu-id="5de9e-110">AVI</span><span class="sxs-lookup"><span data-stu-id="5de9e-110">AVI</span></span>
- <span data-ttu-id="5de9e-111">CS</span><span class="sxs-lookup"><span data-stu-id="5de9e-111">CS</span></span>
- <span data-ttu-id="5de9e-112">CSS</span><span class="sxs-lookup"><span data-stu-id="5de9e-112">CSS</span></span>
- <span data-ttu-id="5de9e-113">DOC</span><span class="sxs-lookup"><span data-stu-id="5de9e-113">DOC</span></span>
- <span data-ttu-id="5de9e-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="5de9e-114">DOCX</span></span>
- <span data-ttu-id="5de9e-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="5de9e-115">EPUB</span></span>
- <span data-ttu-id="5de9e-116">GIF</span><span class="sxs-lookup"><span data-stu-id="5de9e-116">GIF</span></span>
- <span data-ttu-id="5de9e-117">INDD</span><span class="sxs-lookup"><span data-stu-id="5de9e-117">INDD</span></span>
- <span data-ttu-id="5de9e-118">JAR</span><span class="sxs-lookup"><span data-stu-id="5de9e-118">JAR</span></span>
- <span data-ttu-id="5de9e-119">JPG</span><span class="sxs-lookup"><span data-stu-id="5de9e-119">JPG</span></span>
- <span data-ttu-id="5de9e-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="5de9e-120">JPEG</span></span>
- <span data-ttu-id="5de9e-121">JS</span><span class="sxs-lookup"><span data-stu-id="5de9e-121">JS</span></span>
- <span data-ttu-id="5de9e-122">MP3</span><span class="sxs-lookup"><span data-stu-id="5de9e-122">MP3</span></span>
- <span data-ttu-id="5de9e-123">MP4</span><span class="sxs-lookup"><span data-stu-id="5de9e-123">MP4</span></span>
- <span data-ttu-id="5de9e-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="5de9e-124">MPEG</span></span>
- <span data-ttu-id="5de9e-125">MPG</span><span class="sxs-lookup"><span data-stu-id="5de9e-125">MPG</span></span>
- <span data-ttu-id="5de9e-126">ODP</span><span class="sxs-lookup"><span data-stu-id="5de9e-126">ODP</span></span>
- <span data-ttu-id="5de9e-127">ODS</span><span class="sxs-lookup"><span data-stu-id="5de9e-127">ODS</span></span>
- <span data-ttu-id="5de9e-128">ODT</span><span class="sxs-lookup"><span data-stu-id="5de9e-128">ODT</span></span>
- <span data-ttu-id="5de9e-129">PDF</span><span class="sxs-lookup"><span data-stu-id="5de9e-129">PDF</span></span>
- <span data-ttu-id="5de9e-130">PNG</span><span class="sxs-lookup"><span data-stu-id="5de9e-130">PNG</span></span>
- <span data-ttu-id="5de9e-131">PPT</span><span class="sxs-lookup"><span data-stu-id="5de9e-131">PPT</span></span>
- <span data-ttu-id="5de9e-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="5de9e-132">PPTX</span></span>
- <span data-ttu-id="5de9e-133">PS</span><span class="sxs-lookup"><span data-stu-id="5de9e-133">PS</span></span>
- <span data-ttu-id="5de9e-134">QXP</span><span class="sxs-lookup"><span data-stu-id="5de9e-134">QXP</span></span>
- <span data-ttu-id="5de9e-135">RAR</span><span class="sxs-lookup"><span data-stu-id="5de9e-135">RAR</span></span>
- <span data-ttu-id="5de9e-136">RTF</span><span class="sxs-lookup"><span data-stu-id="5de9e-136">RTF</span></span>
- <span data-ttu-id="5de9e-137">SVG</span><span class="sxs-lookup"><span data-stu-id="5de9e-137">SVG</span></span>
- <span data-ttu-id="5de9e-138">TAR</span><span class="sxs-lookup"><span data-stu-id="5de9e-138">TAR</span></span>
- <span data-ttu-id="5de9e-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="5de9e-139">TGZ</span></span>
- <span data-ttu-id="5de9e-140">TXT</span><span class="sxs-lookup"><span data-stu-id="5de9e-140">TXT</span></span>
- <span data-ttu-id="5de9e-141">WMV</span><span class="sxs-lookup"><span data-stu-id="5de9e-141">WMV</span></span>
- <span data-ttu-id="5de9e-142">XLS</span><span class="sxs-lookup"><span data-stu-id="5de9e-142">XLS</span></span>
- <span data-ttu-id="5de9e-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="5de9e-143">XLSX</span></span>
- <span data-ttu-id="5de9e-144">XML</span><span class="sxs-lookup"><span data-stu-id="5de9e-144">XML</span></span>
- <span data-ttu-id="5de9e-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="5de9e-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="5de9e-146">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="5de9e-146">Upload a file</span></span>

<span data-ttu-id="5de9e-147">หากต้องการอัพโหลดไฟล์ไปยังโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="5de9e-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5de9e-148">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="5de9e-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="5de9e-149">บนแถบคำสั่ง เลือก **อัพโหลด \> อัพโหลดรายการสื่อ**</span><span class="sxs-lookup"><span data-stu-id="5de9e-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="5de9e-150">ในตัวสำรวจไฟล์ ให้เลือกไฟล์ตั้งแต่หนึ่งไฟล์ขึ้นไป แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="5de9e-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="5de9e-151">ในกล่องโต้ตอบ **อัพโหลดรายการสื่อ** ให้ป้อนชื่อเรื่อง คำอธิบาย และข้อมูลเมตาของคำสำคัญ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="5de9e-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="5de9e-152">เมื่อต้องการเผยแพร่ไฟล์หลังจากการอัพโหลดโดยทันที ให้เลือกกล่องกาเครื่องหมาย **เผยแพร่รายการสื่อหลังจากการอัพโหลด**</span><span class="sxs-lookup"><span data-stu-id="5de9e-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="5de9e-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="5de9e-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5de9e-154">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5de9e-154">Additional resources</span></span>

[<span data-ttu-id="5de9e-155">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="5de9e-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="5de9e-156">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="5de9e-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="5de9e-157">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="5de9e-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="5de9e-158">ตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="5de9e-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="5de9e-159">กำหนดค่าจุดโฟกัสของภาพ</span><span class="sxs-lookup"><span data-stu-id="5de9e-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
