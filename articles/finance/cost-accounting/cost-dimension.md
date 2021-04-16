---
title: สร้างมิติและนำเข้าสมาชิกมิติ
description: การบัญชีต้นทุนคือโมดูลอิสระที่กำหนดให้ต้องมีข้อมูลหลักจากโมดูลอื่น
author: ShylaThompson
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a9634612bcffbcf71b77dbb184e71367c67bac10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822938"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="c8bc2-103">สร้างมิติและนำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="c8bc2-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8bc2-104">การบัญชีต้นทุนคือโมดูลอิสระที่กำหนดให้ต้องมีข้อมูลจากโมดูลอื่น</span><span class="sxs-lookup"><span data-stu-id="c8bc2-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="c8bc2-105">ข้อมูลนี้แบ่งออกได้ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="c8bc2-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="c8bc2-106">องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-106">Cost elements</span></span>
-  <span data-ttu-id="c8bc2-107">ออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-107">Cost objects</span></span>
-  <span data-ttu-id="c8bc2-108">มิติทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="c8bc2-108">Statistical dimensions</span></span>

<span data-ttu-id="c8bc2-109">**องค์ประกอบต้นทุน** สอดคล้องกับรายการต้นทุนที่เกี่ยวข้องในผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="c8bc2-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="c8bc2-110">**ออบเจ็กต์ต้นทุน** สอดคล้องกับชนิดของมิติทางการเงินใด ๆ เช่น ผลิตภัณฑ์ ศูนย์ต้นทุน และโครงการที่คุณต้องการประเมิน ปันส่วนต้นทุนไปยัง หรือวัดโดยตรง</span><span class="sxs-lookup"><span data-stu-id="c8bc2-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="c8bc2-111">**มิติทางสถิติ** และสมาชิกถูกใช้ในการลงทะเบียนรายการที่ไม่ใช่เงินตรา</span><span class="sxs-lookup"><span data-stu-id="c8bc2-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="c8bc2-112">สมาชิกของมิติทางสถิติสามารถใช้เป็นฐานการปันส่วนในการกระจายต้นทุน และการปันส่วนต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="c8bc2-113">แผนภาพต่อไปนี้แสดงให้เห็นถึงมิติที่ใช้ในการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="c8bc2-114">[![มิติการบัญชีต้นทุน](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="c8bc2-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="c8bc2-115">หลังจากที่นำเข้าข้อมูลลงในการบัญชีต้นทุน คุณสามารถใช้เพื่อสร้างมุมมองต่าง ๆ ที่ให้ข้อมูลเชิงลึกกับผู้จัดการในทุกระดับขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c8bc2-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="c8bc2-116">หัวข้อต่อไปนี้แสดงข้อมูลเกี่ยวกับการสร้างมิติและนำเข้าสมาชิกมิติ</span><span class="sxs-lookup"><span data-stu-id="c8bc2-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="c8bc2-117">มิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="c8bc2-118">สร้างองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="c8bc2-119">มิติออบเจ็กต์ต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="c8bc2-120">แม็ปสมาชิกมิติองค์ประกอบต้นทุนไปยังชุดทั่วไปของมิติ</span><span class="sxs-lookup"><span data-stu-id="c8bc2-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="c8bc2-121">แม็ปมิติองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="c8bc2-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="c8bc2-122">สมาชิกมิติทางสถิติและเท็มเพลตตัวให้บริการการประเมินทางสถิติ</span><span class="sxs-lookup"><span data-stu-id="c8bc2-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]