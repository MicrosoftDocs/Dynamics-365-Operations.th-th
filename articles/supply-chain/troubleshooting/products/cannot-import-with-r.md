---
title: คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2
description: คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026941"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="6930b-103">คุณไม่สามารถนําเข้าสินค้าโดยใช้เอนทิตีผลิตภัณฑ์ที่นําออกใช้ V2</span><span class="sxs-lookup"><span data-stu-id="6930b-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="6930b-104">หมายเลข KB: 4611825</span><span class="sxs-lookup"><span data-stu-id="6930b-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="6930b-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="6930b-105">Symptoms</span></span>

<span data-ttu-id="6930b-106">เมื่อคุณพยายามนําเข้าสินค้าโดยใช้เอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2* คุณจะได้รับข้อความแสดงข้อผิดพลาดที่คล้ายกับตัวอย่างต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6930b-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="6930b-107">ไม่สามารถสร้างเรกคอร์ดในสินค้า - กลุ่มมิติการติดตาม (EcoResTrackingDimensionGroupItem)</span><span class="sxs-lookup"><span data-stu-id="6930b-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="6930b-108">หมายเลขสินค้า: 2040663, ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6930b-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="6930b-109">มีเรกคอร์ดอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="6930b-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="6930b-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="6930b-110">Resolution</span></span>

<span data-ttu-id="6930b-111">เมื่อต้องการนําเข้าผลิตภัณฑ์ที่นําออกใช้ใหม่ คุณต้องใช้เอนทิตี *การสร้างผลิตภัณฑ์ที่นําออกใช้ V2* แทนเอนทิตี *ผลิตภัณฑ์ที่นําออกใช้ V2*</span><span class="sxs-lookup"><span data-stu-id="6930b-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
