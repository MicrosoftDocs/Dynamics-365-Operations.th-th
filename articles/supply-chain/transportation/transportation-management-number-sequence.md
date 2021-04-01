---
title: ลำดับหมายเลขการจัดการการขนส่ง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าลำดับหมายเลขสำหรับการจัดการการขนส่ง
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
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233378"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="2f218-103">ลำดับหมายเลขการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2f218-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f218-104">ใช้หน้า **ลำดับหมายเลข** ในโมดูลการจัดการการขนส่งเพื่อตั้งค่าตัวเลขที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="2f218-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="2f218-105">หมายเลข Pro ใช้โดยผู้ขนส่งเพื่อจัดระเบียบและติดตามความคืบหน้าของการจัดส่งสินค้าแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="2f218-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="2f218-106">การสร้างลำดับหมายเลขสำหรับหมายเลข Pro</span><span class="sxs-lookup"><span data-stu-id="2f218-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="2f218-107">เมื่อต้องการสร้างลำดับหมายเลขสำหรับหมายเลข Pro ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f218-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="2f218-108">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ลำดับหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="2f218-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="2f218-109">เลือก **สร้าง** เพื่อสร้างลำดับหมายเลขใหม่</span><span class="sxs-lookup"><span data-stu-id="2f218-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="2f218-110">ป้อนรหัสเฉพาะและชื่อช่วยอธิบายสำหรับลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="2f218-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="2f218-111">ในฟิลด์ **ชนิดลำดับหมายเลข** *หมายเลข Pro* เป็นตัวเลือกเดียว</span><span class="sxs-lookup"><span data-stu-id="2f218-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="2f218-112">ในฟิลด์ **ตัวเลขการตรวจสอบ** *ตัวเลขการตรวจสอบ* มีเพียงตัวเลือกเดียวและตั้งค่าเป็นกลไกจัดการทั่วไป</span><span class="sxs-lookup"><span data-stu-id="2f218-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="2f218-113">บนแท็บด่วน **ลำดับ** ให้ข้อมูลเกี่ยวกับลำดับ</span><span class="sxs-lookup"><span data-stu-id="2f218-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="2f218-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2f218-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="2f218-115">การเชื่อมโยงลำดับหมายเลขกับผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="2f218-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="2f218-116">เมื่อต้องการเชื่อมโยงลำดับหมายเลขกับผู้ขนส่ง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="2f218-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="2f218-117">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> ผู้ขนส่งสินค้า**</span><span class="sxs-lookup"><span data-stu-id="2f218-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="2f218-118">เลือกผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="2f218-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="2f218-119">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="2f218-119">Select **Edit**.</span></span>
1. <span data-ttu-id="2f218-120">บนแท็บด่วน **ภาพรวม** ให้เลือกตัวเลือกในฟิลด์ **ลำดับหมายเลข Pro**</span><span class="sxs-lookup"><span data-stu-id="2f218-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="2f218-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2f218-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]