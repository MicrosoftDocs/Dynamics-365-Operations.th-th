---
title: ตั้งค่าคอนฟิกชื่อโดเมนของคุณ
description: หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096831"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="f31c4-103">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="f31c4-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f31c4-104">หัวข้อนี้จะอธิบายถึงวิธีการตั้งค่าคอนฟิกชื่อโดเมนสำหรับไซต์อีคอมเมิร์ซ Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f31c4-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="f31c4-105">เพิ่มโดเมนระหว่างการเริ่มต้นอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f31c4-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="f31c4-106">เมื่อต้องการเชื่อมโยงโดเมนกับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ ให้เริ่มต้นการใช้อีคอมเมิร์ซตามที่อธิบายไว้ใน [การจัดวางไซต์ e commerce ใหม่](deploy-ecommerce-site.md)</span><span class="sxs-lookup"><span data-stu-id="f31c4-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="f31c4-107">ระหว่างการเริ่มต้น ระบบจะขอให้คุณป้อนข้อมูลที่จะใช้เพื่อจัดเตรียมสภาพแวดล้อมของอีคอมเมิร์ซของคุณ</span><span class="sxs-lookup"><span data-stu-id="f31c4-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="f31c4-108">ในฟิลด์ **ชื่อโฮสต์ที่ได้รับการสนับสนุน** ให้เพิ่มโดเมนทั้งหมดที่คุณวางแผนที่จะใช้กับสภาพแวดล้อมการทำงานนี้</span><span class="sxs-lookup"><span data-stu-id="f31c4-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="f31c4-109">โดเมนต่างๆ ควรถูกแยกด้วยเครื่องหมายอัฒภาค</span><span class="sxs-lookup"><span data-stu-id="f31c4-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="f31c4-110">ในลักษณะนี้จะมีการตั้งค่าคอนฟิกโดเมนในส่วนประกอบอีคอมเมิร์ซทั้งหมดที่จำเป็น และจะพร้อมใช้งานเมื่อคุณสลับปริมาณการใช้งานจากเครือข่ายการจัดส่งเนื้อหา (CDN) หรือเว็บเซิร์ฟเวอร์ของคุณ แล้วชี้ไปที่ฟรอนท์เอนด์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f31c4-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="f31c4-111">เพิ่มโดเมนหลังจากการเริ่มต้นอีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f31c4-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="f31c4-112">เมื่อต้องการเชื่อมโยงโดเมนใหม่กับสภาพแวดล้อมของอีคอมเมิร์ซของคุณ หลังจากการเริ่มต้นอีคอมเมิร์ซคุณต้องส่งคำขอบริการ</span><span class="sxs-lookup"><span data-stu-id="f31c4-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f31c4-113">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f31c4-113">Additional resources</span></span>

[<span data-ttu-id="f31c4-114">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="f31c4-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f31c4-115">ตั้งค่าช่องทางร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="f31c4-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="f31c4-116">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="f31c4-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f31c4-117">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f31c4-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f31c4-118">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="f31c4-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="f31c4-119">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="f31c4-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f31c4-120">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="f31c4-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f31c4-121">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f31c4-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f31c4-122">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="f31c4-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f31c4-123">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="f31c4-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f31c4-124">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="f31c4-124">Enable location-based store detection</span></span>](enable-store-detection.md)
