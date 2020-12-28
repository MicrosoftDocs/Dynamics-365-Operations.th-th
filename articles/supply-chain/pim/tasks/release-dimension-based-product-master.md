---
title: นำผลิตภัณฑ์หลักที่ใช้มิติออกใช้
description: 'ขั้นตอนนี้แสดงวิธีการนำออกใช้ผลิตภัณฑ์หลักซึ่งจะใช้สำหรับการจัดโครงแบบตามมิติ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd207d202c24ced9e29bdfc7386fb6464a838a0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438334"
---
# <a name="release-a-dimension-based-product-master"></a><span data-ttu-id="a0d41-103">นำผลิตภัณฑ์หลักที่ใช้มิติออกใช้</span><span class="sxs-lookup"><span data-stu-id="a0d41-103">Release a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0d41-104">ขั้นตอนนี้แสดงวิธีการนำออกใช้ผลิตภัณฑ์หลักซึ่งจะใช้สำหรับการจัดโครงแบบตามมิติ </span><span class="sxs-lookup"><span data-stu-id="a0d41-104">This procedure shows how to release a product master, which will be used for the dimension-based configurations.</span></span> <span data-ttu-id="a0d41-105">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="a0d41-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a0d41-106">นี่คือข้อกำหนดเบื้องต้นที่คุณได้สร้างผลิตภัณฑ์หลักด้วยเทคโนโลยีการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a0d41-106">It is a prerequisite that you have created a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="a0d41-107">นี่เป็นกระบวนงานที่สองจากแปดกระบวนงาน ซึ่งอธิบายถึงวิธีการสร้างชุดสำหรับการจัดโครงแบบตามมิติ</span><span class="sxs-lookup"><span data-stu-id="a0d41-107">This is the second procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="a0d41-108">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก </span><span class="sxs-lookup"><span data-stu-id="a0d41-108">Go to Product information management > Products > Product masters.</span></span>
    * <span data-ttu-id="a0d41-109">ตัวกรองคอลัมน์เทคโนโลยีการจัดโครงดังนั้นจะแสดงการจัดโครงแบบตามมิติเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="a0d41-109">Filter the Configuration technology column so that only the dimension-based configuration is displayed.</span></span> <span data-ttu-id="a0d41-110">ตัวอย่างเช่น คุณสามารถกรองคอลัมน์โดยการพิมพ์มิติ</span><span class="sxs-lookup"><span data-stu-id="a0d41-110">For example, you can filter the column by typing Dimension.</span></span>    
2. <span data-ttu-id="a0d41-111">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0d41-111">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="a0d41-112">คลิกนำออกใช้ผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="a0d41-112">Click Release products.</span></span>
4. <span data-ttu-id="a0d41-113">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a0d41-113">Click Next.</span></span>
    * <span data-ttu-id="a0d41-114">สำหรับผลิตภัณฑ์ที่ถูกสร้างด้วยเทคโนโลยีการตั้งค่าคอนฟิกตามมิติ ผลิตภัณฑ์ย่อยต้องถูกสร้างในบริษัทที่จะมีสร้างสูตรการผลิต </span><span class="sxs-lookup"><span data-stu-id="a0d41-114">For products that are crated with the dimension-based configuration technology, the product variants must be created in the company where the bill of materials will be created.</span></span>  
5. <span data-ttu-id="a0d41-115">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a0d41-115">Click Next.</span></span>
6. <span data-ttu-id="a0d41-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a0d41-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a0d41-117">เลือกบริษัท USMF สำหรับกระบวนงานนี้ </span><span class="sxs-lookup"><span data-stu-id="a0d41-117">Select the company USMF for this procedure.</span></span>  
7. <span data-ttu-id="a0d41-118">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="a0d41-118">Click Next.</span></span>
8. <span data-ttu-id="a0d41-119">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="a0d41-119">Click Finish.</span></span>

