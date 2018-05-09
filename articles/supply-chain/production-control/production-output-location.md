---
title: "ที่ตั้งเอาท์พุทการผลิต"
description: "หัวข้อนี้อธิบายถึงลำดับชั้นที่ใช้ในการระบุที่ตั้งเอาท์พุทการผลิต"
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ef820db6cdb2ce485ded0dbca9635af5c68403c6
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="production-output-location"></a><span data-ttu-id="9a7cd-103">ที่ตั้งเอาท์พุทการผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a7cd-104">หัวข้อนี้อธิบายถึงลำดับชั้นที่ใช้ในการระบุที่ตั้งเอาท์พุทการผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="9a7cd-105">ที่ตั้งเอาท์พุทการผลิตคือ สถานที่จัดเก็บสินค้าสำเร็จรูปหลังจากผ่านกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="9a7cd-106">โดยปกติ สถานที่เก็บนี้จะอยู่ในบริเวณใกล้เคียงกับกระบวนการผลิตที่ใช้ผลิตสินค้าสำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="9a7cd-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="9a7cd-107">ที่ตั้งเอาท์พุทการผลิตจะใช้เป็นที่เก็บระหว่างกลางสำหรับวัสดุ ก่อนที่จะย้ายในกับพื้นที่การจัดส่ง สถานที่จัดเก็บ สถานที่ตั้งอินพุทการผลิตสำหรับกระบวนการผลิตปลายน้ำ และต่อไป</span><span class="sxs-lookup"><span data-stu-id="9a7cd-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="9a7cd-108">ที่ตั้งเอาท์พุทการผลิตเริ่มต้นจะถูกกำหนดเมื่อมีรายงานการผลิตสินค้าสำเร็จรูปในใบสั่งผลิตหรือใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="9a7cd-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="9a7cd-109">จะใช้ลำดับชั้นต่อไปนี้ในการระบุที่ตั้งเอาท์พุทนี้:</span><span class="sxs-lookup"><span data-stu-id="9a7cd-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="9a7cd-110">ใช้ที่ตั้งเอาท์พุทที่กำหนดในหัวข้อใบสั่งผลิตหรือใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="9a7cd-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="9a7cd-111">ถ้าไม่มีที่ตั้งในหัวข้อใบสั่งผลิตหรือใบสั่งชุดงาน ระบบจะใช้ที่ตั้งเอาท์พุทที่กำหนดในทรัพยากรที่ใช้โดยการดำเนินงานล่าสุดที่กำหนดไว้ในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="9a7cd-112">ถ้ายังไม่พบที่ตั้งอีก ระบบจะใช้ที่ตั้งเอาท์พุทที่กำหนดในกลุ่มทรัพยากรที่ใช้โดยทรัพยากรสำหรับการดำเนินงานล่าสุดที่กำหนดไว้ในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="9a7cd-113">ถ้ายังไม่พบที่ตั้งอีก ระบบจะใช้ที่ตั้งเอาท์พุทที่กำหนดในคลังสินค้าที่กำหนดไว้สำหรับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="9a7cd-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="9a7cd-114">ที่ตั้งเอาท์พุทการผลิตเริ่มต้นได้รับการกำหนดเอาไว้สำหรับผลิตภัณฑ์ที่มีการตั้งค่าโดยใช้กระบวนการคลังสินค้าขั้นสูงเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9a7cd-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="9a7cd-115">เมื่อมีรายงานว่าสินค้าชนิดนี้เสร็จสมบูรณ์ ชนิดงานคลังสินค้าสำหรับ **การสำรองสินค้าที่สำเร็จแล้ว** หรือ **การสำรองสินค้าที่สำเร็จแล้ว** จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="9a7cd-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="9a7cd-116">ชนิดงานนี้ใช้ที่ตั้งเอาท์พุทการผลิตเป็นสถานที่เบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="9a7cd-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="9a7cd-117">สถานที่ย้ายเก็บจะถูกกำหนดโดยคำสั่งสถานที่</span><span class="sxs-lookup"><span data-stu-id="9a7cd-117">The put-away location is determined by the location directives.</span></span>

