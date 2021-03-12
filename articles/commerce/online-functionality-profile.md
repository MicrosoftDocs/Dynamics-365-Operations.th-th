---
title: สร้างโปรไฟล์ฟังก์ชันการทำงานออนไลน์
description: หัวข้อนี้อธิบายวิธีสร้างโปรไฟล์ฟังก์ชันการทำงานออนไลน์ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969987"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="5dedf-103">สร้างโปรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5dedf-104">หัวข้อนี้นำเสนอภาพรวมในการตั้งค่าโปรไฟล์ฟังก์ชันการทำงานออนไลน์สำหรับ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5dedf-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5dedf-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="5dedf-105">Overview</span></span>

<span data-ttu-id="5dedf-106">โปรไฟล์ฟังก์ชันการทำงานออนไลน์ได้ให้การตั้งค่าต่างๆที่ใช้สำหรับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="5dedf-107">แต่ละช่องทางออนไลน์ต้องระบุโปรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="5dedf-108">สร้างโปรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-108">Create an online functionality profile</span></span>

<span data-ttu-id="5dedf-109">กระบวนการต่อไปนี้อธิบายวิธีสร้างโปรไฟล์ฟังก์ชันการทำงานออนไลน์จากภายในแอปสำนักงานใหญ่การค้า</span><span class="sxs-lookup"><span data-stu-id="5dedf-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="5dedf-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การตั้งค่าช่องทาง \> การตั้งร้านค้าออนไลน์ \> โปรไฟล์ฟังก์ชันการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="5dedf-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="5dedf-111">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="5dedf-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5dedf-112">ในฟิลด์ **โปรไฟล์** ให้ป้อนรหัสสำหรับโปรไฟล์</span><span class="sxs-lookup"><span data-stu-id="5dedf-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="5dedf-113">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า ("โพรไฟล์ Adventure Works" ในรูปภาพตัวอย่างด้านล่าง)</span><span class="sxs-lookup"><span data-stu-id="5dedf-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="5dedf-114">ในส่วน **ฟังก์ชั่น** ปรับเปลี่ยนการตั้งค่า **รถเข็นสินค้า**, **ลูกค้าการขายปลีก** หรือ **เช็คเอาท์** ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="5dedf-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="5dedf-115">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="5dedf-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5dedf-116">ภาพต่อไปนี้แสดงตัวอย่างของโปรไฟล์ฟังก์ชันการทำงานออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-116">The following image shows an example online functionality profile.</span></span>
  
![ตัวอย่างของโปรไฟล์ฟังก์ชันการทำงานออนไลน์](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="5dedf-118">ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="5dedf-118">Functions</span></span>

- <span data-ttu-id="5dedf-119">**ผลิตภัณฑ์รวม**: เมื่อเปิดใช้งาน ฟังก์ชั่นนี้จะช่วยให้รถเข็นปรับปรุงปริมาณเมื่อมีการเพิ่มรายการเดียวกันหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="5dedf-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="5dedf-120">**อนุญาตให้ชำระเงินแบบไม่มีการชำระเงิน**: เมื่อเปิดใช้งาน ฟังก์ชั่นนี้จะจัดการกับสถานการณ์เมื่อรายการที่เพิ่มลงในรถเข็นมีราคา $0.00 </span><span class="sxs-lookup"><span data-stu-id="5dedf-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="5dedf-121">**สร้างลูกค้าในโหมดอะซิงโครนัส**: นี่เป็นการตั้งค่าดั้งเดิมที่ใช้กับช่องทาง e-Commerce บุคคลที่ภายนอกและไม่สามารถใช้ได้กับไซต์ e-Commerce Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5dedf-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5dedf-122">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5dedf-122">Additional resources</span></span>

[<span data-ttu-id="5dedf-123">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5dedf-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5dedf-124">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="5dedf-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5dedf-125">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="5dedf-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="5dedf-126">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="5dedf-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="5dedf-127">ตั้งค่าช่องทางศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="5dedf-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
