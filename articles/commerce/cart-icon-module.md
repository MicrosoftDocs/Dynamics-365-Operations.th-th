---
title: โมดูลไอคอนรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261592"
---
# <a name="cart-icon-module"></a><span data-ttu-id="6f5d4-103">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f5d4-104">หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6f5d4-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f5d4-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="6f5d4-105">Overview</span></span>

<span data-ttu-id="6f5d4-106">โมดูลไอคอนรถเข็นแสดงถึงรถเข็นในส่วนหัวของหน้าและแสดงจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="6f5d4-107">โมดูลไอคอนรถเข็นยังแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="6f5d4-108">รถเข็นแบบมินิให้ผู้ใช้ได้รับสรุปของสินค้าในรถเข็นโดยไม่ต้องนำทางไปยังหน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="6f5d4-109">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถไปยังหน้าการเช็คเอาท์โดยตรงหากพอใจกับสรุป</span><span class="sxs-lookup"><span data-stu-id="6f5d4-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="6f5d4-110">การทำเช่นนี้จะช่วยลดจำนวนการนำทางของหน้าและทำการเช็คเอาท์ได้รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="6f5d4-111">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="6f5d4-111">Module properties</span></span>

- <span data-ttu-id="6f5d4-112">**แสดงรถเข็นแบบมินิ** – เมื่อเป็นจริง คุณสมบัตินี้จะเปิดใช้งานสรุปรถเข็น (รถเข็นมินิ) ที่จะแสดงเมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="6f5d4-113">ฟังก์ชันนี้ได้รับการสนับสนุนสำหรับพอร์ตมุมมองเดสก์ท็อปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="6f5d4-114">เพิ่มโมดูลไอคอนรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="6f5d4-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="6f5d4-115">เมื่อต้องการเพิ่มโมดูลไอคอนรถเข็น ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="6f5d4-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6f5d4-116">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6f5d4-116">Additional resources</span></span>

[<span data-ttu-id="6f5d4-117">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6f5d4-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6f5d4-118">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="6f5d4-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6f5d4-119">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="6f5d4-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6f5d4-120">โมดูลการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="6f5d4-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6f5d4-121">โมดูหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="6f5d4-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6f5d4-122">โมดูลของส่วนท้าย</span><span class="sxs-lookup"><span data-stu-id="6f5d4-122">Footer module</span></span>](author-footer-module.md)
