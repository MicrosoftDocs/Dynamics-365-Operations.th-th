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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 138c256b56593c4fafb20050a97e614fa584597c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997839"
---
# <a name="cart-icon-module"></a><span data-ttu-id="b30bc-103">โมดูลไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b30bc-104">หัวข้อนี้ครอบคลุมถึงโมดูลไอคอนรถเข็นและอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b30bc-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b30bc-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b30bc-105">Overview</span></span>

<span data-ttu-id="b30bc-106">โมดูลไอคอนรถเข็นแสดงถึงรถเข็นในส่วนหัวของหน้าและแสดงจำนวนของสินค้าในรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="b30bc-107">โมดูลไอคอนรถเข็นยังแสดงสรุปรถเข็น (หรือที่เรียกอีกอย่างหนึ่งว่ารถเข็นมินิ) เมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="b30bc-108">รถเข็นแบบมินิให้ผู้ใช้ได้รับสรุปของสินค้าในรถเข็นโดยไม่ต้องนำทางไปยังหน้ารถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="b30bc-109">นอกจากนี้ยังช่วยให้ผู้ใช้สามารถไปยังหน้าการเช็คเอาท์โดยตรงหากพอใจกับสรุป</span><span class="sxs-lookup"><span data-stu-id="b30bc-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="b30bc-110">การทำเช่นนี้จะช่วยลดจำนวนการนำทางของหน้าและทำการเช็คเอาท์ได้รวดเร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="b30bc-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="b30bc-111">การสนับสนุนสำหรับโมดูลไอคอนรถเข็นมีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.11</span><span class="sxs-lookup"><span data-stu-id="b30bc-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="b30bc-112">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลไอคอนรถเข็นที่แสดงรถเข็นมินิในส่วนหัวของ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="b30bc-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![ตัวอย่างของโมดูลไอคอนรถเข็น](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="b30bc-114">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="b30bc-114">Module properties</span></span>

- <span data-ttu-id="b30bc-115">**แสดงรถเข็นแบบมินิ** – เมื่อเป็นจริง คุณสมบัตินี้จะเปิดใช้งานสรุปรถเข็น (รถเข็นมินิ) ที่จะแสดงเมื่อวางเมาส์เหนือไอคอนรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="b30bc-116">ฟังก์ชันนี้ได้รับการสนับสนุนสำหรับพอร์ตมุมมองเดสก์ท็อปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b30bc-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="b30bc-117">เพิ่มโมดูลไอคอนรถเข็นไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="b30bc-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="b30bc-118">เมื่อต้องการเพิ่มโมดูลไอคอนรถเข็น ให้ดูที่ [โมดูลส่วนหัว](author-header-module.md)</span><span class="sxs-lookup"><span data-stu-id="b30bc-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b30bc-119">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b30bc-119">Additional resources</span></span>

[<span data-ttu-id="b30bc-120">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="b30bc-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b30bc-121">โมดูลเช็คเอาท์</span><span class="sxs-lookup"><span data-stu-id="b30bc-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b30bc-122">โมดูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b30bc-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b30bc-123">โมดูลที่อยู่ที่จัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b30bc-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b30bc-124">โมดูลตัวเลือกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b30bc-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b30bc-125">โมดูลข้อมูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="b30bc-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b30bc-126">โมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b30bc-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b30bc-127">โมดูลบัตรของขวัญ</span><span class="sxs-lookup"><span data-stu-id="b30bc-127">Gift card module</span></span>](add-giftcard.md)
