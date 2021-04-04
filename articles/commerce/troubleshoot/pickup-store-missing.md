---
title: ร้านค้าปลีกไม่มีอยู่ในรายการร้านค้าที่จะเบิกสินค้า
description: หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อร้านค้าปลีกไม่ปรากฏในรายการร้านค้าที่สามารถเบิกสินค้าได้
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585562"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="fd304-103">ร้านค้าปลีกไม่มีอยู่ในรายการร้านค้าที่จะเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fd304-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd304-104">หัวข้อนี้มีการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อร้านค้าปลีกไม่ปรากฏในรายการร้านค้าที่สามารถเบิกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="fd304-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="fd304-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="fd304-105">Description</span></span>

<span data-ttu-id="fd304-106">ร้านค้าปลีกไม่ปรากฏในรายการร้านค้าที่สามารถเบิกสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="fd304-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="fd304-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="fd304-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="fd304-108">ตั้งค่าคอนฟิกลองติจูดและละติจูดของที่อยู่ร้านค้าในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="fd304-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="fd304-109">เพื่อตั้งค่าคอนฟิกลองติจูดและละติจูดของที่อยู่ร้านค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="fd304-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fd304-110">ไปยัง **Retail และ Commerce \> ช่องทาง \> ร้านค้า \> ร้านค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="fd304-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="fd304-111">ค้นหาร้านค้าที่คุณต้องการให้ปรากฏในตัวเลือกการเบิกสินค้าบนไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="fd304-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="fd304-112">บันทึกค่า **หมายเลขหน่วยปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="fd304-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="fd304-113">ไปที่ **การจัดการองค์กร \>องค์กร \>หน่วยปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="fd304-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="fd304-114">ค้นหาหมายเลขหน่วยปฏิบัติงานที่คุณระบุไว้ก่อนหน้านี้ แล้วเลือกหน่วยปฏิบัติงานในผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fd304-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="fd304-115">บนแท็บด่วน **ที่อยู่** ให้เลือก **ตัวเลือกเพิ่มเติม** แล้วเลือก **ขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="fd304-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="fd304-116">บนแท็บด่วน **ทั่วไป** ให้ตรวจสอบให้แน่ใจว่าได้ตั้งค่าฟิลด์ **ลองติจูด** และ **ละติจูด** อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fd304-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="fd304-117">ในส่วนของขั้นตอนนี้ ให้ตรวจสอบให้แน่ใจว่าได้ระบุค่าเป็นตัวเลขค่าบวกหรือค่าลบอย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="fd304-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="fd304-118">ตั้งค่าคอนฟิกกลุ่มการเติมสินค้าในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="fd304-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="fd304-119">หากต้องการตั้งค่าคอนฟิกกลุ่มการเติมสินค้าในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="fd304-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="fd304-120">ไปที่ **การค้าปลึกและการพาณิชย์ \> ช่องทางการขาย \> ร้านค้าออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="fd304-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="fd304-121">เลือกร้านค้าออนไลน์ที่จะตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fd304-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="fd304-122">ในบานหน้าต่างการดำเนินการ ให้เลือกแท็บ **การตั้งค่า** และจากนั้นเลือก **การกำหนดกลุ่มการเติมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="fd304-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="fd304-123">บนหน้า **การมอบหมายกลุ่มการเติมสินค้า** ให้เลือกกลุ่มการเติมสินค้าของร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="fd304-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="fd304-124">ภายใต้ **การตั้งค่า** ตรวจสอบให้แน่ใจว่าร้านค้าปลีกได้รับการตั้งค่าคอนฟิกสำหรับกลุ่มการเติมสินค้าอย่างถูกต้องแล้ว</span><span class="sxs-lookup"><span data-stu-id="fd304-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd304-125">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd304-125">Additional resources</span></span> 

[<span data-ttu-id="fd304-126">สร้างหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="fd304-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="fd304-127">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="fd304-127">Set up an online channel</span></span>](../channel-setup-online.md)
