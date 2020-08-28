---
title: โมดูลไอคอนรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661158"
---
# <a name="cart-icon-module"></a><span data-ttu-id="fd979-103">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd979-104">หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="fd979-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd979-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="fd979-105">Overview</span></span>

<span data-ttu-id="fd979-106">โมดูลไอคอนรถเข็นแสดงถึงรถเข็นในส่วนหัวของหน้าและแสดงจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="fd979-107">โมดูลไอคอนรถเข็นยังแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="fd979-108">รถเข็นแบบมินิให้ผู้ใช้ได้รับสรุปของสินค้าในรถเข็นโดยไม่ต้องนำทางไปยังหน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="fd979-109">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถไปยังหน้าการเช็คเอาท์โดยตรงหากพอใจกับสรุป</span><span class="sxs-lookup"><span data-stu-id="fd979-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="fd979-110">การทำเช่นนี้จะช่วยลดจำนวนการนำทางของหน้าและทำการเช็คเอาท์ได้รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd979-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="fd979-111">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลไอคอนรถเข็นที่แสดงรถเข็นมินิในส่วนหัวของ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="fd979-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![ตัวอย่างของโมดูลไอคอนรถเข็น](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="fd979-113">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="fd979-113">Module properties</span></span>

- <span data-ttu-id="fd979-114">**แสดงรถเข็นแบบมินิ** – เมื่อเป็นจริง คุณสมบัตินี้จะเปิดใช้งานสรุปรถเข็น (รถเข็นมินิ) ที่จะแสดงเมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="fd979-115">ฟังก์ชันนี้ได้รับการสนับสนุนสำหรับพอร์ตมุมมองเดสก์ท็อปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="fd979-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="fd979-116">เพิ่มโมดูลไอคอนรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="fd979-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="fd979-117">เมื่อต้องการเพิ่มโมดูลไอคอนรถเข็น ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="fd979-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd979-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd979-118">Additional resources</span></span>

[<span data-ttu-id="fd979-119">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="fd979-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd979-120">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="fd979-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fd979-121">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fd979-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fd979-122">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fd979-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fd979-123">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fd979-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fd979-124">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="fd979-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fd979-125">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="fd979-125">Gift card module</span></span>](add-giftcard.md)
