---
title: วิธีการแบบแผนการคิดค่าเสื่อมราคาแบบครึ่งปี
description: หัวข้อนี้จะอธิบายวิธีการที่สินทรัพย์ถาวรใช้ในการคำนวณค่าเสื่อมราคาโดยใช้แบบแผนครึ่งปี ซึ่งจะคำนวณค่าเสื่อมราคาหกเดือนระหว่างปีแรกและปีสุดท้ายในการใช้งานของสินทรัพย์
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d0e33128c37e970ebf5af87bd601ae30aef96952
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818595"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="be240-103">วิธีการแบบแผนการคิดค่าเสื่อมราคาแบบครึ่งปี</span><span class="sxs-lookup"><span data-stu-id="be240-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="be240-104">หัวข้อนี้จะอธิบายวิธีการที่ใช้ในสินทรัพย์ถาวรเพื่อคำนวณค่าเสื่อมราคาโดยใช้แบบแผนครึ่งปี</span><span class="sxs-lookup"><span data-stu-id="be240-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="be240-105">แบบแผนครึ่งปีจะคำนวณค่าเสื่อมราคาแบบหกเดือนระหว่างปีแรกและปีสุดท้ายในการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="be240-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="be240-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับแบบแผนการคิดค่าเสื่อมราคา ดูที่ [วิธีการคิดค่าเสื่อมราคาและแบบแผนการคิดค่าเสื่อมราคา](Fixed-asset-depreciation-conventions.md)</span><span class="sxs-lookup"><span data-stu-id="be240-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="be240-107">เมื่อคุณใช้แบบแผนการคิดค่าเสื่อมราคาหกเดือน ระบบจะใช้ปีการซื้อสินทรัพย์หรือปีที่มีการใช้งานสินทรัพย์ แล้วจึงคำนวณค่าเสื่อมราคาห้าปีจากปีนั้นแล้วเพิ่มไปอีกหกเดือน</span><span class="sxs-lookup"><span data-stu-id="be240-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="be240-108">เมื่อต้องการแสดงให้เห็นถึงกระบวนการนี้ ให้พิจารณาสินทรัพย์ที่ได้รับมาจากราคา 50,000 และระบุไว้ในการใช้งานเดือนเมษายน 2020</span><span class="sxs-lookup"><span data-stu-id="be240-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="be240-109">นอกจากนี้ สมมติว่าสินทรัพย์มีอายุการใช้งานห้าปี</span><span class="sxs-lookup"><span data-stu-id="be240-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="be240-110">ปีแรกของการใช้งานจะสรุปในเดือนธันวาคม 2020 ซึ่งหมายความว่าการสิ้นสุดของอายุการใช้งานห้าปีของสินทรัพย์จะเป็นเดือนธันวาคม 2024</span><span class="sxs-lookup"><span data-stu-id="be240-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="be240-111">แบบแผนการคิดค่าเสื่อมราคาครึ่งปีจะเพิ่มอายุของสินทรัพย์ไปอีก 6 เดือน ซึ่งหมายความว่าอายุการใช้งานจะสิ้นสุดในเดือนมิถุนายน 2025</span><span class="sxs-lookup"><span data-stu-id="be240-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="be240-112">ค่าเสื่อมราคาต่อปี 50,000/5 = 10,000 ค่าเสื่อมราคาต่อเดือน 10,000/12 = 833.33</span><span class="sxs-lookup"><span data-stu-id="be240-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="be240-113">ค่าเสื่อมราคาในปีแรก 10,000/2 = 5,000 และค่าเสื่อมราคาต่อเดือนต่อมา 5,000/9 = 555.56</span><span class="sxs-lookup"><span data-stu-id="be240-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="be240-114">[![กำหนดการคิดค่าเสื่อมราคาสำหรับแบบแผนการคิดค่าเสื่อมราคาครึ่งปี](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="be240-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="be240-115">รอบระยะเวลาการคิดค่าเสื่อมราคาแบบขยายที่บวกเพิ่มตามแบบแผนครึ่งปีจะมีการปันส่วนค่าเสื่อมราคาที่ถูกต้องมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="be240-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="be240-116">แบบแผนหกเดือนแสดงถึงค่าใช้จ่ายของค่าเสื่อมราคาที่เท่ากันมากขึ้น ซึ่งจะมีประโยชน์สำหรับการรายงานในงบกำไรขาดทุน</span><span class="sxs-lookup"><span data-stu-id="be240-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]