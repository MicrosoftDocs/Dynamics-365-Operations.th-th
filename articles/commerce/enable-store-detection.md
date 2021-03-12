---
title: เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง
description: หัวข้อนี้จะอธิบายวิธีการเปิดการตรวจสอบร้านค้าตามสถานที่สำหรับไซต์ Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000740"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="179b2-103">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="179b2-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="179b2-104">หัวข้อนี้จะอธิบายวิธีการเปิดการตรวจสอบร้านค้าตามสถานที่สำหรับไซต์ Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="179b2-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="179b2-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="179b2-105">Overview</span></span>

<span data-ttu-id="179b2-106">การตรวจสอบร้านค้าตามสถานที่ใน Commerce ช่วยให้คุณสามารถให้เนื้อหาไซต์ที่เกี่ยวข้องแก่ลูกค้าตามสถานที่ของของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="179b2-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="179b2-107">เมื่อมีการเปิดใช้งานการตรวจสอบร้านค้าตามสถานที่ให้บริการการแสดงผล Commerce จะใช้ข้อมูลประเทศ/ภูมิภาคจากที่อยู่ IP ของเว็บเบราเซอร์ของลูกค้า เพื่อส่งงลูกค้าไปที่การตั้งค่าคอนฟิกไซต์ทางภูมิศาสตร์ที่ดีที่สุดซึ่งพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="179b2-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="179b2-108">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="179b2-108">Privacy notice</span></span>

<span data-ttu-id="179b2-109">ถ้าคุณเปิดใช้งานลักษณะการทำงานการตรวจหาร้านค้าตามสถานที่ข้อมูลจากเบราว์เซอร์ของลูกค้าจะถูกส่งไปยังบริการที่ตั้งของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="179b2-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="179b2-110">ข้อมูลนี้จะใช้เพื่อให้เนื้อหาของลูกค้าที่เกี่ยวข้องกับสถานที่ของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="179b2-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="179b2-111">ข้อมูลทั้งสองที่ส่งมาจากเบราว์เซอร์ของลูกค้าและข้อมูลตามสถานที่ที่ส่งคืนให้กับลูกค้าต้องเป็นไปตามนโยบายการปฏิบัติตามกฎระเบียบและคุกกี้</span><span class="sxs-lookup"><span data-stu-id="179b2-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="179b2-112">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="179b2-112">Turn on location-based store detection</span></span>

<span data-ttu-id="179b2-113">เมื่อต้องการเปิดใช้งานการตรวจสอบร้านค้าตามสถานที่ใน Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="179b2-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="179b2-114">ในเครื่องมือการสร้าง ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="179b2-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="179b2-115">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **การจัดการไซต์**</span><span class="sxs-lookup"><span data-stu-id="179b2-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="179b2-116">เลือก **การตั้งค่าไซต์**</span><span class="sxs-lookup"><span data-stu-id="179b2-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="179b2-117">ตั้งค่าตัวเลือก **เปิดใช้งานการตรวจสอบร้านค้าตามสถานที่** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="179b2-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="179b2-118">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="179b2-118">Additional resources</span></span>

[<span data-ttu-id="179b2-119">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="179b2-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="179b2-120">ปรับใช้ผู้เช่าอีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="179b2-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="179b2-121">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="179b2-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="179b2-122">เชื่อมโยงไซต์ Dynamics 365 Commerce กับช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="179b2-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="179b2-123">จัดการไฟล์ robots.txt</span><span class="sxs-lookup"><span data-stu-id="179b2-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="179b2-124">อัพโหลดการเปลี่ยนเส้นทาง URL จำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="179b2-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="179b2-125">ตั้งค่าผู้เช่า B2C ใน Commerce</span><span class="sxs-lookup"><span data-stu-id="179b2-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="179b2-126">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="179b2-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="179b2-127">ตั้งค่าคอนฟิกผู้เช่า B2C หลายรายในสภาพแวดล้อม Commerce</span><span class="sxs-lookup"><span data-stu-id="179b2-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="179b2-128">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="179b2-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
