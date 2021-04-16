---
title: 'สถานะการจัดการการขนส่ง:'
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างสถานะการขนส่งและแม็ปสถานะกับสถานะของผู้ขนส่ง
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807619"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="40fb5-103">สถานะการจัดการการขนส่ง:</span><span class="sxs-lookup"><span data-stu-id="40fb5-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40fb5-104">ตั้งค่ารหัสหลักสำหรับสถานะการขนส่งเพื่อแปลรหัสที่ระบุโดยผู้ขนส่งสินค้าของคุณ</span><span class="sxs-lookup"><span data-stu-id="40fb5-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="40fb5-105">การทำเช่นนี้จะช่วยให้คุณสามารถรวมกับผู้ขนส่งที่ให้สถานะ</span><span class="sxs-lookup"><span data-stu-id="40fb5-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="40fb5-106">สถานะการขนส่งที่คุณให้ไว้สำหรับรหัสสถานะหลักขนส่งสามารถช่วยให้คุณติดตามสถานะของการผลิต จัดส่ง หรือคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="40fb5-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="40fb5-107">สถานะการขนส่งเฉพาะสำหรับการผลิต การจัดส่ง หรือคอนเทนเนอร์สามารถอัพเดตได้โดยใช้การรวมข้อมูลเท่านั้นและไม่ผ่านอินเทอร์เฟสผู้ใช้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="40fb5-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="40fb5-108">สร้างสถานะการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-108">Create a transportation status</span></span>

<span data-ttu-id="40fb5-109">เมื่อต้องการสร้างสถานะการขนส่ง ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="40fb5-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="40fb5-110">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ต้นแบบสถานะการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="40fb5-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="40fb5-111">เลือก **สร้าง** เพื่อสร้างต้นแบบสถานะการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="40fb5-112">ในฟิลด์ **ต้นแบบสถานะการขนส่ง** ให้ป้อนรหัสเฉพาะสำหรับสถานะการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="40fb5-113">ในฟิลด์ **ชนิดการขนส่ง** เลือก *ผู้ขนส่ง* หรือ *ฮับ* เป็นชนิดของการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="40fb5-114">ป้อนชื่อและสถานะการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="40fb5-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="40fb5-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="40fb5-116">การแม็ปสถานะการขนส่งไปยังสถานะของผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="40fb5-117">หากต้องการแม็ปสถานะการขนส่งไปยังสถานะของผู้ขนส่ง ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="40fb5-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="40fb5-118">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> ผู้ขนส่ง \> สถานะการขนส่งของผู้ขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="40fb5-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="40fb5-119">เลือก **สร้าง** เพื่อแม็ปรหัสจากผู้ขนส่งไปยังรหัสหลักของสถานะการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="40fb5-120">เลือกรหัสเฉพาะสำหรับผู้ขนส่งสินค้าและบริการผู้ขนส่ง</span><span class="sxs-lookup"><span data-stu-id="40fb5-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="40fb5-121">เลือกรหัสสถานะการขนส่งที่คุณต้องการแม็ปกับรหัสผู้ขนส่งของที่เลือก</span><span class="sxs-lookup"><span data-stu-id="40fb5-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="40fb5-122">ป้อนรหัสภายนอกที่ใช้โดยผู้ขนส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="40fb5-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="40fb5-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="40fb5-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]