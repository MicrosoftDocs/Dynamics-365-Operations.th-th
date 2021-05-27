---
title: ใบสั่งซื้อจะไม่แสดงข้อความผลิตภัณฑ์ที่แปล
description: ใบสั่งซื้อจะไม่แสดงข้อความผลิตภัณฑ์ที่แปล
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, SysTranslationDetail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9b0f5ceec89327e11ce895b4de159c8e4317ec2b
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026936"
---
# <a name="purchase-orders-dont-show-translated-product-text"></a><span data-ttu-id="28539-103">ใบสั่งซื้อจะไม่แสดงข้อความผลิตภัณฑ์ที่แปล</span><span class="sxs-lookup"><span data-stu-id="28539-103">Purchase orders don't show translated product text</span></span>

<span data-ttu-id="28539-104">หมายเลข KB: 4612098</span><span class="sxs-lookup"><span data-stu-id="28539-104">KB number: 4612098</span></span>

## <a name="symptoms"></a><span data-ttu-id="28539-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="28539-105">Symptoms</span></span>

<span data-ttu-id="28539-106">คุณได้กําหนดการแปลข้อความเป็นชื่อผลิตภัณฑ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="28539-106">You've defined text translations for product names.</span></span> <span data-ttu-id="28539-107">อย่างไรก็ตาม ชื่อผลิตภัณฑ์จะแสดงในภาษาดั้งเดิมเสมอ โดยไม่พิจารณาการตั้งค่าภาษาในแอป</span><span class="sxs-lookup"><span data-stu-id="28539-107">However, product names are always shown in the original language, regardless of the language setting in the app.</span></span>

## <a name="resolution"></a><span data-ttu-id="28539-108">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="28539-108">Resolution</span></span>

<span data-ttu-id="28539-109">การแปลผลิตภัณฑ์จะแสดงขึ้นบนเอกสารที่เชื่อมต่อกับภายนอกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="28539-109">Product translations are shown only on external-facing documents.</span></span> <span data-ttu-id="28539-110">ไม่แสดงแก่ผู้ใช้ภายใน</span><span class="sxs-lookup"><span data-stu-id="28539-110">They aren't shown to internal users.</span></span> <span data-ttu-id="28539-111">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [FAQ เกี่ยวกับการแปลที่เกี่ยวข้องกับผลิตภัณฑ์](../../pim/translations-product-related-information.md#where-can-i-view-the-translated-information)</span><span class="sxs-lookup"><span data-stu-id="28539-111">For more information, see [Product-related translations FAQ](../../pim/translations-product-related-information.md#where-can-i-view-the-translated-information).</span></span>
