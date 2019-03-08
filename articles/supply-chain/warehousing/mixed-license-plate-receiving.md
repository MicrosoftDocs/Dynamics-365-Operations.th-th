---
title: การรับป้ายทะเบียนแบบผสม
description: หัวข้อนี้อธิบายวิธีการใช้การรับป้ายทะเบียนแบบผสมในการลงทะเบียนและสร้างงานสำหรับสินค้าหลายรายการกับอุปกรณ์เคลื่อนที่
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44165bc59d65a9dfdf8e591152f427b97930b34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "365902"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="0df72-103">การรับป้ายทะเบียนแบบผสม</span><span class="sxs-lookup"><span data-stu-id="0df72-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0df72-104">การรับป้ายทะเบียนแบบผสมช่วยให้คุณสร้างป้ายทะเบียนที่ประกอบด้วยสินค้าหลายรายการ ก่อนที่คุณจะลงทะเบียนและสร้างงานสำรอง</span><span class="sxs-lookup"><span data-stu-id="0df72-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="0df72-105">ป้ายทะเบียนที่ประกอบด้วยสินค้าหลายรายการไม่จำเป็นต้องมีการแบ่ง ณ ท่ารับสินค้าเพื่อที่จะลงทะเบียนสินค้าแต่ละรายการสำหรับคุณ</span><span class="sxs-lookup"><span data-stu-id="0df72-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="0df72-106">เมื่อใช้ขั้นตอนที่เกี่ยวข้องกับสินค้าเพื่อระบุรายการเอกสารต้นทาง คุณสามารถสแกนบาร์โค้ดในส่วนการควบคุมสินค้า</span><span class="sxs-lookup"><span data-stu-id="0df72-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="0df72-107">หากบาร์โค้ดมีปริมาณและหน่วยวัด (UOM) ตั้งค่าคอนฟิกไว้แล้ว สินค้าและปริมาณจะถูกเพิ่มไปยังป้ายทะเบียนแบบผสมโดยอัตโนมัติ และจะพาคุณกลับไปยังหน้าจอเพื่อสแกนสินค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="0df72-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="0df72-108">ซึ่งช่วยให้คุณสามารถสแกนสินค้าทั้งหมดได้อย่างรวดเร็ว โดยไม่ต้องทำการยืนยันในแต่ละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="0df72-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="0df72-109">ในขั้นตอนของการรับป้ายทะเบียนแบบผสม คุณสามารถแสดงรายการของสินค้าที่ถูกสแกนไปยังป้ายทะเบียน และจากจุดนี้ คุณสามารถปรับเปลี่ยนหรือแก้ไขปริมาณของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="0df72-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="0df72-110">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="0df72-110">Where it applies</span></span>

<span data-ttu-id="0df72-111">การรับป้ายทะเบียนแบบผสมเป็นขั้นตอนการรับบนอุปกรณ์เคลื่อนที่เพื่อลงทะเบียนและสร้างงานสำหรับรายการ/สินค้าหลายรายการในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="0df72-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="0df72-112">ซึ่งมีประโยชน์ถ้าคุณรับป้ายทะเบียนขาเข้ากับสินค้าหลายรายการ</span><span class="sxs-lookup"><span data-stu-id="0df72-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="0df72-113">วิธีการตั้งค่าการรับป้ายทะเบียนแบบผสม</span><span class="sxs-lookup"><span data-stu-id="0df72-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="0df72-114">มีการตั้งค่าการรับป้ายทะเบียนแบบผสมให้เป็นรายการเมนูบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0df72-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="0df72-115">คุณต้องสร้างรายการเมนูใหม่พร้อมกับงานของโหมดที่ไม่ได้ใช้งานที่มีอยู่ และใช้หนึ่งในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0df72-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="0df72-116">การรับป้ายทะเบียนแบบผสม</span><span class="sxs-lookup"><span data-stu-id="0df72-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="0df72-117">การรับป้ายทะเบียนแบบผสมและการสำรองสินค้า</span><span class="sxs-lookup"><span data-stu-id="0df72-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="0df72-118">ตัวเลือกในการระบุรายการเอกสารต้นทางเป็น สินค้าของใบสั่งซื้อ รายการของใบสั่งซื้อ ใบสั่งส่งคืนสินค้า สินค้าตามใบสั่งโอนย้าย และรายการใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="0df72-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="0df72-119">ตัวเลือกเหล่านี้สามารถเปลี่ยนใบสั่งรับสินค้าบนป้ายทะเบียนแบบเดียวได้</span><span class="sxs-lookup"><span data-stu-id="0df72-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="0df72-120">ตัวเลือกสุดท้ายจะเป็นสินค้าของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="0df72-120">The last option is by load item.</span></span> <span data-ttu-id="0df72-121">คุณสามารถเพิ่มสินค้าหลายรายการไปยังป้ายทะเบียน แต่คุณจะไม่สามารถสลับไปมาระหว่างการบรรทุกหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="0df72-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
