---
title: รวมน้ำหนักตู้บรรจุสินค้าและปริมาตรของสินค้า
description: หัวข้อนี้อธิบายวิธีการตั้งค่าและใช้ฟังก์ชันในการรวมน้ำหนักตู้บรรจุสินค้าและปริมาตรของสินค้า
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549232"
---
# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="9e6f6-103">รวมน้ำหนักตู้บรรจุสินค้าและปริมาตรของสินค้า</span><span class="sxs-lookup"><span data-stu-id="9e6f6-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e6f6-104">ฟังก์ชันสำหรับการรวมน้ำหนักตู้บรรจุสินค้าและปริมาตรของสินค้าแสดงภาพของน้ำหนักรวมและปริมาตรของตู้บรรจุสินค้าและสินค้าที่กำลังจะโหลดได้อย่างชัดเจน</span><span class="sxs-lookup"><span data-stu-id="9e6f6-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="9e6f6-105">จำนวนงานในศูนย์การผลิตประกอบด้วยการจัดส่งครั้งเดียวหรือการจัดส่งหลายครั้ง และการจัดส่งเหล่านี้ประกอบด้วยสินค้าที่แตกต่างกันที่อยู่ในใบสั่งขายใบเดียวหรือใบสั่งขายหลายใบ</span><span class="sxs-lookup"><span data-stu-id="9e6f6-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="9e6f6-106">สินค้าถูกจัดเก็บอยู่ภายในตู้บรรจุสินค้า และตู้บรรจุสินค้าจะถูกโหลดไปยังสินค้า</span><span class="sxs-lookup"><span data-stu-id="9e6f6-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="9e6f6-107">สินค้าที่อยู่นอกตู้บรรจุสินค้าอาจเป็นส่วนหนึ่งของสินค้า</span><span class="sxs-lookup"><span data-stu-id="9e6f6-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="9e6f6-108">ระบบจะคำนวณค่าสำหรับน้ำหนักและปริมาตรของสินค้าโดยขึ้นอยู่กับเงื่อนไขเหล่านี้ โดยพิจารณาถึงน้ำหนักและปริมาตรของทั้งตู้บรรจุสินค้าและสินค้า</span><span class="sxs-lookup"><span data-stu-id="9e6f6-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="9e6f6-109">ถ้าค่าที่คำนวณได้ไม่ชัดเจน คุณสามารถปรับปรุงได้โดยการป้อนค่าที่แท้จริงสำหรับน้ำหนักและปริมาตรของจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="9e6f6-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="9e6f6-110">ค่าสำหรับน้ำหนักและปริมาตรจะถูกใช้ในกระบวนการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9e6f6-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="9e6f6-111">ตัวอย่างเช่น ค่าจะถูกใช้ในเวิร์กเบนช์กระบวนการผลิตอัตรา ซึ่งจะช่วยกำหนดอัตราและกระบวนการผลิตสำหรับสินค้า และยังใช้สำหรับวิธีการชำระเงินการขนส่งและการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9e6f6-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="9e6f6-112">ตำแหน่งที่ใช้</span><span class="sxs-lookup"><span data-stu-id="9e6f6-112">Where it applies</span></span>

<span data-ttu-id="9e6f6-113">ฟังก์ชันสำหรับการรวมน้ำหนักตู้บรรจุสินค้าและปริมาตรของสินค้าจะใช้ในการจัดการกระบวนการขนส่ง เช่น เวิร์กเบนช์กระบวนการผลิตอัตรา วิธีการชำระเงินการขนส่ง และการเช็คอินของพนักงานขนส่ง</span><span class="sxs-lookup"><span data-stu-id="9e6f6-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="9e6f6-114">วิธีตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9e6f6-114">How it is set up</span></span>

<span data-ttu-id="9e6f6-115">หมายเลขของตู้บรรจุสินค้าที่ควรพิจารณาสำหรับสินค้าจะถูกคำนวณตามน้ำหนัก และปริมาตรของตู้บรรจุสินค้า และเปอร์เซ็นต์ของตู้บรรจุสินค้าจะถูกนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="9e6f6-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="9e6f6-116">เมื่อต้องการกำหนดน้ำหนักและปริมาตรสำหรับตู้บรรจุสินค้า ให้คลิก **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **ตู้บรรจุสินค้า** \> **ชนิดของตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9e6f6-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="9e6f6-117">เมื่อต้องการตั้งค่าเปอร์เซ็นต์การใช้ประโยชน์ของตู้บรรจุสินค้า คลิก **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **ตู้บรรจุสินค้า** \> **กลุ่มตู้บรรจุสินค้า** แล้วป้อนค่าในฟิลด์ **เปอร์เซ็นต์การใช้ประโยชน์ของตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9e6f6-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>
