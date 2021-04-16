---
title: ผลิตภัณฑ์และประเภทจะไม่ปรากฏในโปรแกรมสร้างไซต์ Commerce หลังจากแม็ปไซต์ใหม่
description: หัวข้อนี้จะแสดงการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทไม่ปรากฏในโปรแกรมสร้างไซต์ Commerce หลังจากแม็ปไซต์ใหม่แล้ว
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3d7cd2274cb447a622f9ffe6f00b1b27ecc7db52
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801590"
---
# <a name="products-and-categories-dont-appear-in-commerce-site-builder-after-a-new-site-is-mapped"></a><span data-ttu-id="f3352-103">ผลิตภัณฑ์และประเภทจะไม่ปรากฏในโปรแกรมสร้างไซต์ Commerce หลังจากแม็ปไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="f3352-103">Products and categories don't appear in Commerce site builder after a new site is mapped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3352-104">หัวข้อนี้จะแสดงการแก้ไขปัญหาเบื้องต้น ซึ่งสามารถช่วยเมื่อผลิตภัณฑ์และประเภทไม่ปรากฏในโปรแกรมสร้างไซต์ Commerce หลังจากแม็ปไซต์ใหม่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f3352-104">This topic provides troubleshooting guidance that can help when products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="description"></a><span data-ttu-id="f3352-105">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f3352-105">Description</span></span>

<span data-ttu-id="f3352-106">ผลิตภัณฑ์และประเภทจะไม่ปรากฏในโปรแกรมสร้างไซต์ Commerce หลังจากแม็ปไซต์ใหม่</span><span class="sxs-lookup"><span data-stu-id="f3352-106">Products and categories don't appear in Commerce site builder after a new site is mapped.</span></span>

## <a name="resolution"></a><span data-ttu-id="f3352-107">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="f3352-107">Resolution</span></span>

### <a name="add-products-to-channel-categories-in-commerce-headquarters"></a><span data-ttu-id="f3352-108">เพิ่มผลิตภัณฑ์ในประเภทช่องทางในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="f3352-108">Add products to channel categories in Commerce headquarters</span></span>

<span data-ttu-id="f3352-109">ในการเพิ่มผลิตภัณฑ์ในประเภทช่องทางในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f3352-109">To add products to channel categories in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f3352-110">ไปยัง **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและแอตทริบิวต์ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="f3352-110">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="f3352-111">ในการนําทางด้านซ้าย ให้เลือกประเภทที่ควรปรากฏในไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f3352-111">In the left navigation, select the category that should appear on the e-commerce site.</span></span>
1. <span data-ttu-id="f3352-112">บนแท็บด่วน **ผลิตภัณฑ์** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f3352-112">On the **Products** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="f3352-113">ในส่วน **ผลิตภัณฑ์ที่มีอยู่** ให้เลือกผลิตภัณฑ์ที่ควรจะปรากฏ แล้วเลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f3352-113">In the **Available Products** section, select the products that should appear, and then select **Add**.</span></span>
1. <span data-ttu-id="f3352-114">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f3352-114">Select **OK**.</span></span>
1. <span data-ttu-id="f3352-115">หลังจากผลิตภัณฑ์ปรากฏขึ้นบนแท็บด่วน **ผลิตภัณฑ์** ให้เลือก **เผยแพร่การอัพเดตช่องทาง** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f3352-115">After the products appear on the **Products** FastTab, select **Publish channel updates** on the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3352-116">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f3352-116">Additional resources</span></span>

[<span data-ttu-id="f3352-117">ตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f3352-117">Configure a channel to use a channel navigation hierarchy</span></span>](../configure-channel-hierarchy.md)
