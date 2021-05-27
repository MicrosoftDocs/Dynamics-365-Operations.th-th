---
title: เรกคอร์ดลูกค้าไม่ปรากฏในศูนย์ควบคุม Commerce
description: หัวข้อนี้มีคำแนะนำการแก้ไขปัญหาซึ่งสามารถช่วยได้เมื่อเรกคอร์ดลูกค้าไม่ปรากฏในศูนย์ควบคุม Commerce ในทันที
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018493"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="5895e-103">เรกคอร์ดลูกค้าไม่ปรากฏในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="5895e-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5895e-104">หัวข้อนี้มีคำแนะนำการแก้ไขปัญหาซึ่งสามารถช่วยได้เมื่อเรกคอร์ดลูกค้าไม่ปรากฏในศูนย์ควบคุม Commerce ในทันที</span><span class="sxs-lookup"><span data-stu-id="5895e-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="5895e-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="5895e-105">Description</span></span>

<span data-ttu-id="5895e-106">เมื่อคุณสร้างเรกคอร์ดลูกค้าใหม่โดยใช้ขั้นตอนการลงทะเบียนในหน้าร้าน e-commerce เรกคอร์ดลูกค้าที่เกี่ยวข้องจะไม่ปรากฏขึ้นทันทีในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="5895e-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="5895e-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="5895e-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="5895e-108">ปิดใช้งานการสร้างลูกค้าในโหมด async</span><span class="sxs-lookup"><span data-stu-id="5895e-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5895e-109">หากคุณปิดใช้งานการสร้างลูกค้าแบบอะซิงโครนัส ประสิทธิภาพของระบบอาจได้รับผลกระทบ เนื่องจากการสร้างแต่ละเรกคอร์ดจะก่อให้เกิดการร้องขอแบบเรียลไทม์ไปยังศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="5895e-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="5895e-110">นอกจากนี้ ถ้าศูนย์ควบคุม Commerce ไม่ทำงาน (ตัวอย่างเช่น ระหว่างขั้นตอนการให้บริการ) ขั้นตอนการสร้างลูกค้าใหม่จะก่อให้เกิดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="5895e-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="5895e-111">เพื่อปิดใช้งานการสร้างลูกค้าในโหมด async ในศูนย์ควบคุม Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5895e-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5895e-112">ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การตั้งค่าร้านค้าออนไลน์ \> โพรไฟล์ฟังก์ชัน** </span><span class="sxs-lookup"><span data-stu-id="5895e-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="5895e-113">หากคุณยังไม่ได้ใช้โพรไฟล์ฟังก์ชันของช่องทางการขายออนไลน์ของคุณ ให้สร้างโพรไฟล์ขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="5895e-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="5895e-114">ตรวจสอบให้แน่ใจว่าทางเลือก **สร้างลูกค้าในโหมด async** ถูกกำหนดเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="5895e-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="5895e-115">ไปที่ **การค้าปลึกและการพาณิชย์ \> ช่องทางการขาย \> ร้านค้าออนไลน์**</span><span class="sxs-lookup"><span data-stu-id="5895e-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="5895e-116">เลือกร้านค้าออนไลน์เพื่อปิดใช้งานการสร้างลูกค้าแบบอะซิงโครนัส</span><span class="sxs-lookup"><span data-stu-id="5895e-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="5895e-117">บนแท็บ **ทั่วไป** ตรวจสอบให้แน่ใจว่าได้ตั้งค่าเขตข้อมูล **โพรไฟล์ฟังก์ชัน** เป็นโพรไฟล์ฟังก์ชันที่คุณใช้กับช่องทางการขายออนไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5895e-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5895e-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5895e-118">Additional resources</span></span>

[<span data-ttu-id="5895e-119">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="5895e-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
