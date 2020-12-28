---
title: การรับประกันในสินทรัพย์และชนิดสินทรัพย์
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการรับประกันในสินทรัพย์และชนิดสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75de9a51560dcd8fea7998425fee14a27e891972
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438622"
---
# <a name="warranties-on-assets-and-asset-types"></a><span data-ttu-id="68a4d-103">การรับประกันในสินทรัพย์และชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="68a4d-103">Warranties on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="68a4d-104">หัวข้อนี้อธิบายวิธีการตั้งค่าการรับประกันในสินทรัพย์และชนิดสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="68a4d-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="68a4d-105">ตั้งค่าการรับประกันในชนิดสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="68a4d-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="68a4d-106">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ชนิดสินทรัพย์** \> **ชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="68a4d-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="68a4d-107">ในบานหน้าต่างด้านซ้าย ให้เลือกชนิดสินทรัพย์ที่จะแนบกับข้อตกลงการรับประกันของผู้จัดจำหน่าย แล้วเลือก **ค่าเริ่มต้นของชนิดสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="68a4d-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="68a4d-108">บนแท็บด่วน **ทั่วไป** ในฟิลด์ **การรับประกันของผู้จัดจำหน่าย** ให้เลือกข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="68a4d-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="68a4d-109">ตั้งค่าการรับประกันในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="68a4d-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="68a4d-110">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="68a4d-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="68a4d-111">เลือกสินทรัพย์แล้วเลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="68a4d-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="68a4d-112">บนแท็บด่วน **ผู้จัดจำหน่าย** ในส่วน **การรับประกันของผู้จัดจำหน่าย** ในฟิลด์ **การรับประกัน** ให้เลือกข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="68a4d-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="68a4d-113">ในฟิลด์ **เริ่มต้นการรับประกัน** และ **สิ้นสุดการับประกัน** ให้เลือกวันที่เริ่มต้นและสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="68a4d-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="68a4d-114">หากมีการเลือกวันที่ในฟิลด์ **เริ่มต้นการรับประกัน** บนใบสั่งงาน การรับประกันจะมีผลบังคับใช้สำหรับใบสั่งงานในวันที่นั้น</span><span class="sxs-lookup"><span data-stu-id="68a4d-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="68a4d-115">เมื่อคุณสร้างใบสั่งงาน ฟิลด์ **เริ่มต้นการรับประกัน** จะถูกตั้งค่าโดยอัตโนมัติเป็นวันที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="68a4d-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="68a4d-116">อย่างไรก็ตาม คุณสามารถเปลี่ยนแปลงวันที่เพื่อให้ถูกต้อง ตัวอย่างเช่น วันที่เริ่มต้นของข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="68a4d-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![หน้าใบสั่งงาน](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="68a4d-118">เมื่อคุณสร้างใบสั่งงานสำหรับสินทรัพย์ที่ครอบคลุมโดยการรับประกันของผู้จัดจำหน่าย หากใบสั่งงานมีวันที่เริ่มต้นที่คาดไว้ระหว่างรอบระยะเวลาการรับประกัน คุณจะได้รับการแจ้งเตือนเกี่ยวกับข้อตกลงการรับประกัน</span><span class="sxs-lookup"><span data-stu-id="68a4d-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="68a4d-119">คุณสามารถยกเลิกใบสั่งงานได้หากต้องการ</span><span class="sxs-lookup"><span data-stu-id="68a4d-119">You can then cancel the work order, as you require.</span></span>
