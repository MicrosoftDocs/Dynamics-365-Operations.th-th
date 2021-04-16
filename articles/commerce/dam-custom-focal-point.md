---
title: กำหนดค่าจุดโฟกัสของภาพ
description: หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 04/14/2020
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
ms.openlocfilehash: 962caff0e8e41487231c6075fa7b2df2a59dca48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799312"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="bb182-103">ปรับแต่งจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bb182-104">หัวข้อนี้จะอธิบายวิธีการปรับแต่งจุดโฟกัสของภาพในโปรแกรมสร้างไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bb182-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="bb182-105">เมื่อมีการอัพโหลดรูปภาพไปยังไลบรารีสื่อของโปรแกรมสร้างไซต์ Commerce ระบบจะพยายามระบุจุดโฟกัสของรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-105">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="bb182-106">ตัวอย่างเช่น ถ้ารูปภาพมีบุคคลอยู่บนนั้น ระบบจะตั้งค่าจุดโฟกัสเป็นหน้าของบุคคลตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="bb182-106">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="bb182-107">ในกรณีส่วนใหญ่ การตั้งค่าจุดโฟกัสโดยอัตโนมัติจะทำงานได้ดีสำหรับ viewports ทั้งหมด แต่บางครั้งคุณอาจต้องการปรับจุดโฟกัสเพื่อให้แน่ใจว่าจะมองเห็นส่วนเฉพาะของรูปภาพเสมอ</span><span class="sxs-lookup"><span data-stu-id="bb182-107">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="bb182-108">กำหนดจุดโฟกัสที่กำหนดเองสำหรับรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-108">Define a custom focal point for an image</span></span>

<span data-ttu-id="bb182-109">เมื่อต้องการกำหนดค่าจุดโฟกัสที่กำหนดเองสำหรับรูปภาพ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bb182-109">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="bb182-110">ในบานหน้าต่างนำทางด้านซ้ายของโปรแกรมสร้างไซต์ Commerce ให้เลือก **ไลบรารีสื่อ**</span><span class="sxs-lookup"><span data-stu-id="bb182-110">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="bb182-111">ในหน้าต่างหลัก เลือกภาพที่คุณต้องการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="bb182-111">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="bb182-112">บนแถบคำสั่ง ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="bb182-112">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="bb182-113">เลือกรูปภาพเพื่อป้อน **โหมดแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="bb182-113">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="bb182-114">ภายใต้ **โหมดแก้ไข** เลือก **เปลี่ยนจุดโฟกัส**</span><span class="sxs-lookup"><span data-stu-id="bb182-114">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="bb182-115">ตัวควบคุมจุดโฟกัสแบบวงกลมจะปรากฏบนรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-115">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="bb182-116">เลือกตัวควบคุมจุดโฟกัสเพื่อเลื่อนไปที่จุดโฟกัสที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bb182-116">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="bb182-117">เมื่อคุณดำเนินการเสร็จสิ้นแล้ว บนแถบคำสั่ง ให้เลือก **บันทึก** และจากนั้น เลือก **เสร็จสิ้นการแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="bb182-117">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb182-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="bb182-118">Additional resources</span></span>

[<span data-ttu-id="bb182-119">ภาพรวมของการจัดการสินทรัพย์ดิจิทัล</span><span class="sxs-lookup"><span data-stu-id="bb182-119">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="bb182-120">อัพโหลดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-120">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="bb182-121">อัพโหลดวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="bb182-121">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="bb182-122">อัพโหลดไฟล์</span><span class="sxs-lookup"><span data-stu-id="bb182-122">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="bb182-123">ครอบตัดรูปภาพ</span><span class="sxs-lookup"><span data-stu-id="bb182-123">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="bb182-124">อัปโหลดและให้บริการไฟล์แบบคงที่</span><span class="sxs-lookup"><span data-stu-id="bb182-124">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
