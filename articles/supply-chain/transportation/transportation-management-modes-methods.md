---
title: วิธีการและวิธีการจัดการการขนส่ง
description: หัวข้อนี้แสดงวิธีการตั้งค่าวิธีการและวิธีการจัดการการขนส่ง
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0d41d8665252a978962bf6a2e307dce3dad64a5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233450"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="dfc13-103">วิธีการและวิธีการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="dfc13-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfc13-104">โหมดการจัดการการขนส่งแสดงชนิดการขนส่งที่ผู้ขนส่งจะใช้สำหรับการขนส่งสินค้าจัดส่ง เช่น น้อยกว่าที่มีการบรรทุก (LTL), Truckload (TL), หรือพัสดุ</span><span class="sxs-lookup"><span data-stu-id="dfc13-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="dfc13-105">วิธีการขนส่งแสดงถึงฟอร์มการขนส่งที่ผู้ขนส่งที่ใช้สำหรับการขนส่งการจัดส่ง เช่น ทางอากาศ ภาคพื้นดิน มหาสมุทร หรือรถไฟ</span><span class="sxs-lookup"><span data-stu-id="dfc13-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="dfc13-106">วิธีการและวิธีการขนส่งจะใช้ในบริบทต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="dfc13-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="dfc13-107">เฉพาะโหมดที่ใช้ในแผนกระบวนการผลิต ในขณะที่โหมดทั้งสองและวิธีการขนส่งใช้เมื่อตั้งค่าผู้ขนส่งและบริการผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="dfc13-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="dfc13-108">ไม่มีความสัมพันธ์หรือลำดับชั้นที่ชัดแจ้งอยู่ระหว่างโหมดและวิธีการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="dfc13-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="dfc13-109">สร้างโหมด</span><span class="sxs-lookup"><span data-stu-id="dfc13-109">Create a mode</span></span>

<span data-ttu-id="dfc13-110">เมื่อต้องการสร้างโหมด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="dfc13-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="dfc13-111">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง > \> โหมด**</span><span class="sxs-lookup"><span data-stu-id="dfc13-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="dfc13-112">เลือก **สร้าง** เพื่อสร้างโหมดใหม่</span><span class="sxs-lookup"><span data-stu-id="dfc13-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="dfc13-113">ป้อนรหัสเฉพาะและชื่อช่วยอธิบายสำหรับโหมด</span><span class="sxs-lookup"><span data-stu-id="dfc13-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="dfc13-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dfc13-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="dfc13-115">สร้างวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="dfc13-115">Create a transportation method</span></span>

<span data-ttu-id="dfc13-116">เมื่อต้องการสร้างวิธีการขนส่ง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="dfc13-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="dfc13-117">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> วิธีการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="dfc13-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="dfc13-118">เลือก **สร้าง** เพื่อสร้างวิธีการขนส่งใหม่</span><span class="sxs-lookup"><span data-stu-id="dfc13-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="dfc13-119">ป้อนรหัสเฉพาะและชื่อช่วยอธิบายสำหรับวิธีการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="dfc13-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="dfc13-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dfc13-120">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]