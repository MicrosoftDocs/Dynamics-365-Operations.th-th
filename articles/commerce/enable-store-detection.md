---
title: เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง
description: หัวข้อนี้จะอธิบายวิธีการเปิดการตรวจสอบร้านค้าตามสถานที่สำหรับไซต์ Dynamics 365 Commerce ของคุณ
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a542d6987280451910b4ff3bcfb3a109a0e028c6
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697623"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="1e26e-103">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="1e26e-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1e26e-104">หัวข้อนี้จะอธิบายวิธีการเปิดการตรวจสอบร้านค้าตามสถานที่สำหรับไซต์ Dynamics 365 Commerce ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1e26e-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="1e26e-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="1e26e-105">Overview</span></span>

<span data-ttu-id="1e26e-106">การตรวจสอบร้านค้าตามสถานที่ใน Commerce ช่วยให้คุณสามารถให้เนื้อหาไซต์ที่เกี่ยวข้องแก่ลูกค้าตามสถานที่ของของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="1e26e-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="1e26e-107">เมื่อมีการเปิดใช้งานการตรวจสอบร้านค้าตามสถานที่ให้บริการการแสดงผล Commerce จะใช้ข้อมูลประเทศ/ภูมิภาคจากที่อยู่ IP ของเว็บเบราเซอร์ของลูกค้า เพื่อส่งงลูกค้าไปที่การตั้งค่าคอนฟิกไซต์ทางภูมิศาสตร์ที่ดีที่สุดซึ่งพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="1e26e-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="1e26e-108">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="1e26e-108">Privacy notice</span></span>

<span data-ttu-id="1e26e-109">ถ้าคุณเปิดใช้งานลักษณะการทำงานการตรวจหาร้านค้าตามสถานที่ข้อมูลจากเบราว์เซอร์ของลูกค้าจะถูกส่งไปยังบริการที่ตั้งของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e26e-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="1e26e-110">ข้อมูลนี้จะใช้เพื่อให้เนื้อหาของลูกค้าที่เกี่ยวข้องกับสถานที่ของเขาหรือเธอ</span><span class="sxs-lookup"><span data-stu-id="1e26e-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="1e26e-111">ข้อมูลทั้งสองที่ส่งมาจากเบราว์เซอร์ของลูกค้าและข้อมูลตามสถานที่ที่ส่งคืนให้กับลูกค้าต้องเป็นไปตามนโยบายการปฏิบัติตามกฎระเบียบและคุกกี้</span><span class="sxs-lookup"><span data-stu-id="1e26e-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="1e26e-112">เปิดใช้งานการตรวจหาร้านค้าตามตำแหน่งที่ตั้ง</span><span class="sxs-lookup"><span data-stu-id="1e26e-112">Turn on location-based store detection</span></span>

<span data-ttu-id="1e26e-113">เมื่อต้องการเปิดใช้งานการตรวจสอบร้านค้าตามสถานที่ใน Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="1e26e-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1e26e-114">ในเครื่องมือการสร้าง ให้ไปที่ไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1e26e-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="1e26e-115">ในบานหน้าต่างนำทางทางด้านซ้าย ให้เลือก **การจัดการไซต์**</span><span class="sxs-lookup"><span data-stu-id="1e26e-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="1e26e-116">เลือก **การตั้งค่าไซต์**</span><span class="sxs-lookup"><span data-stu-id="1e26e-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="1e26e-117">ตั้งค่าตัวเลือก **เปิดใช้งานการตรวจสอบร้านค้าตามสถานที่** เป็น **เปิด**</span><span class="sxs-lookup"><span data-stu-id="1e26e-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e26e-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="1e26e-118">Additional resources</span></span>

[<span data-ttu-id="1e26e-119">ภาพรวมของร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="1e26e-119">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="1e26e-120">สร้างไซต์อีคอมเมิร์ซ</span><span class="sxs-lookup"><span data-stu-id="1e26e-120">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1e26e-121">ปรับใช้ไซต์อีคอมเมิร์ซใหม่</span><span class="sxs-lookup"><span data-stu-id="1e26e-121">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1e26e-122">เชื่อมโยงไซต์ออนไลน์กับช่องทาง</span><span class="sxs-lookup"><span data-stu-id="1e26e-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="1e26e-123">ตั้งค่าคอนฟิกชื่อโดเมนของคุณ</span><span class="sxs-lookup"><span data-stu-id="1e26e-123">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="1e26e-124">เพิ่มการสนับสนุนสำหรับเครือข่ายการจัดส่งเนื้อหา (CDN)</span><span class="sxs-lookup"><span data-stu-id="1e26e-124">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1e26e-125">ตั้งค่าหน้าแบบกำหนดเองสำหรับการล็อกอินของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="1e26e-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
