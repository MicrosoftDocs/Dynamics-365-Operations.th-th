---
title: สร้างโพรไฟล์ฟังก์ชันของการขายปลีก
description: หัวข้อนี้จะอธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันของการขายปลีกใหม่ Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002854"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="cb00d-103">สร้างโพรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cb00d-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cb00d-104">หัวข้อนี้จะอธิบายวิธีการสร้างโพรไฟล์ฟังก์ชันของการขายปลีกใหม่ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cb00d-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cb00d-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="cb00d-105">Overview</span></span>

<span data-ttu-id="cb00d-106">โพรไฟล์ฟังก์ชันของการขายปลีก มอบความสามารถในการตั้งค่าต่าง ๆ ที่ใช้สำหรับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb00d-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="cb00d-107">ช่องทางการขายปลีกแต่ละช่องต้องระบุโพรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cb00d-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="cb00d-108">สร้างโพรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cb00d-108">Create a retail functionality profile</span></span>

<span data-ttu-id="cb00d-109">เมื่อต้องการสร้างโพรไฟล์ฟังก์ชันของการขายปลีก ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cb00d-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="cb00d-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> ตั้งค่าช่องทาง \> โพรไฟล์ POS \> โพรไฟล์ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="cb00d-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="cb00d-111">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cb00d-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="cb00d-112">ในฟิลด์ **โพรไฟล์** ให้ป้อนรหัสของโพรไฟล์ ("FN006" ในรูปภาพตัวอย่างด้านล่าง)</span><span class="sxs-lookup"><span data-stu-id="cb00d-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="cb00d-113">ในฟิลด์ **คำอธิบาย** ให้ป้อนค่า ("โพรไฟล์ Adventure Works" ในรูปภาพตัวอย่างด้านล่าง)</span><span class="sxs-lookup"><span data-stu-id="cb00d-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="cb00d-114">ในส่วน **ทั่วไป** ให้เลือกประเทศสำหรับระบบภาษา **ISO**</span><span class="sxs-lookup"><span data-stu-id="cb00d-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="cb00d-115">ในส่วน **ทั่วไป** ให้แก้ไขการตั้งค่าอื่น ๆ ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb00d-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="cb00d-116">ในส่วน **ทั่วไป** ให้เลือก **รหัสโพรไฟล์ใบเสร็จ** สำหรับใบเสร็จทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="cb00d-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="cb00d-117">ในส่วน **ฟังก์ชัน** ให้แก้ไขการตั้งค่าตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb00d-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="cb00d-118">ในส่วน **จำนวน** ให้แก้ไขการตั้งค่าตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb00d-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="cb00d-119">ในส่วน **รหัสข้อมูล** ให้แก้ไขการตั้งค่าตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb00d-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="cb00d-120">ในส่วน **การกำหนดหมายเลขใบเสร็จ** ให้แก้ไขการตั้งค่าตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb00d-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="cb00d-121">รูปภาพต่อไปนี้แสดงตัวอย่างของโพรไฟล์ฟังก์ชันของการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="cb00d-121">The following image shows an example retail functionality profile.</span></span>
  
![ตัวอย่างโพรไฟล์ฟังก์ชันของการขายปลีก](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="cb00d-123">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cb00d-123">Additional resources</span></span>

[<span data-ttu-id="cb00d-124">รหัสข้อมูลและกลุ่มรหัสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="cb00d-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="cb00d-125">สร้างสมุดที่อยู่ใหม่</span><span class="sxs-lookup"><span data-stu-id="cb00d-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="cb00d-126">ภาพรวมโครงร่างหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="cb00d-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="cb00d-127">ตั้งค่าคอนฟิกและติดตั้ง Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="cb00d-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
