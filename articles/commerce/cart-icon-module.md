---
title: โมดูลไอคอนรถเข็น
description: หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 4ab1609d332b96c0588b06aa086dd4fee944e5d9
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055771"
---
# <a name="cart-icon-module"></a><span data-ttu-id="32c86-103">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32c86-104">หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="32c86-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32c86-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="32c86-105">Overview</span></span>

<span data-ttu-id="32c86-106">โมดูลไอคอนรถเข็นแสดงถึงรถเข็นในส่วนหัวของหน้าและแสดงจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="32c86-107">โมดูลไอคอนรถเข็นยังแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="32c86-108">รถเข็นแบบมินิให้ผู้ใช้ได้รับสรุปของสินค้าในรถเข็นโดยไม่ต้องนำทางไปยังหน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="32c86-109">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถไปยังหน้าการเช็คเอาท์โดยตรงหากพอใจกับสรุป</span><span class="sxs-lookup"><span data-stu-id="32c86-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="32c86-110">การทำเช่นนี้จะช่วยลดจำนวนการนำทางของหน้าและทำการเช็คเอาท์ได้รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="32c86-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="32c86-111">การสนับสนุนสำหรับโมดูลไอคอนรถเข็นมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="32c86-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="32c86-112">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลไอคอนรถเข็นที่แสดงรถเข็นมินิในส่วนหัวของ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="32c86-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![ตัวอย่างของโมดูลไอคอนรถเข็น](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="32c86-114">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="32c86-114">Module properties</span></span>

- <span data-ttu-id="32c86-115">**แสดงรถเข็นแบบมินิ** – เมื่อเป็นจริง คุณสมบัตินี้จะเปิดใช้งานสรุปรถเข็น (รถเข็นมินิ) ที่จะแสดงเมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="32c86-116">ฟังก์ชันนี้ได้รับการสนับสนุนสำหรับพอร์ตมุมมองเดสก์ท็อปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="32c86-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="32c86-117">เพิ่มโมดูลไอคอนรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="32c86-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="32c86-118">เมื่อต้องการเพิ่มโมดูลไอคอนรถเข็น ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="32c86-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32c86-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="32c86-119">Additional resources</span></span>

[<span data-ttu-id="32c86-120">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="32c86-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="32c86-121">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="32c86-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="32c86-122">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="32c86-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="32c86-123">โมดูลที่อยู่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="32c86-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="32c86-124">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="32c86-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="32c86-125">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="32c86-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="32c86-126">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="32c86-126">Gift card module</span></span>](add-giftcard.md)
