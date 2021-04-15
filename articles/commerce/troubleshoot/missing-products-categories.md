---
title: ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801734"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="90092-103">ผลิตภัณฑ์และประเภทขาดหายไปหลังจากการคัดลอกสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="90092-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90092-104">หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทขาดหายไปหลังจากที่คัดลอกไซต์ระหว่างสภาพแวดล้อมหรือภายในสภาพแวดล้อมเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="90092-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="90092-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="90092-105">Description</span></span>

<span data-ttu-id="90092-106">หลังจากคัดลอกไซต์จากสภาพแวดล้อมหนึ่งไปยังอีกสภาพแวดล้อมหนึ่ง หรือในสภาพแวดล้อมเดียวกัน ผลิตภัณฑ์และประเภทขาดหายไปจากไซต์</span><span class="sxs-lookup"><span data-stu-id="90092-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="90092-107">ผลิตภัณฑ์และประเภทขาดหายไปจากหน้าร้านอีคอมเมิร์ซและจากแท็บ **ผลิตภัณฑ์** ในโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="90092-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="90092-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="90092-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="90092-109">แม็ปหมายเลขหน่วยปฏิบัติงานของช่องทางกับไซต์ที่คัดลอกใหม่ของโปรแกรมสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="90092-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="90092-110">ในการแม็ปหมายเลขหน่วยปฏิบัติงาน (OUN) ของช่องทางกับไซต์ที่คัดลอกใหม่ของโปรแกรมสร้างไซต์ Commerce ทำตามขั้นตอนดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="90092-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="90092-111">เลือกไซต์ที่คัดลอกใหม่</span><span class="sxs-lookup"><span data-stu-id="90092-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="90092-112">ด้านล่าง **การตั้งค่าไซต์** เลือก **ช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="90092-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="90092-113">ถัดจากชื่อช่องทาง ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เปลี่ยนช่องทางร้านค้าออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="90092-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="90092-114">ในกล่องโต้ตอบ **เปลี่ยนช่องทางร้านค้าออนไลน์** เลือกช่องทางที่จะแม็ปไปยังไซต์ที่คัดลอกใหม่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="90092-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="90092-115">เลือก **Save and publish**</span><span class="sxs-lookup"><span data-stu-id="90092-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90092-116">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="90092-116">Additional resources</span></span>

[<span data-ttu-id="90092-117">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="90092-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
