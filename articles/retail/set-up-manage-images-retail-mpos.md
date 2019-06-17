<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-manage-images-retail-mpos.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-manage-images-retail-mpos.3cc4ad.c256569135a00ea98a5c059b9dd12a07a000ee6a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c256569135a00ea98a5c059b9dd12a07a000ee6a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\set-up-manage-images-retail-mpos.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่าและจัดการรูปภาพสำหรับ Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บทความนี้อธิบายขั้นตอนที่เกี่ยวข้องในการตั้งค่า และการจัดการรูปภาพสำหรับหน่วยงานต่างๆ ที่ปรากฏขึ้นใน Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่าและจัดการรูปภาพสำหรับ Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บทความนี้อธิบายขั้นตอนที่เกี่ยวข้องในการตั้งค่า และการจัดการรูปภาพสำหรับหน่วยงานต่างๆ ที่ปรากฏขึ้นใน Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Setting up the media base URL and defining media templates to configure the format for image URLs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การตั้งค่าฐานสื่อ URL และการกำหนดเท็มเพลตสื่อเพื่อตั้งค่าคอนฟิกรูปแบบสำหรับ URL ของรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The images that appear in Retail Modern POS (MPOS) must be hosted externally, outside Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รูปภาพที่ปรากฏใน Retail Modern POS(MPOS) ต้องถูกโฮสต์ภายนอก นอก Microsoft Dynamics 365 for Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Typically, they are hosted in a content management system, content delivery network (CDN), or media server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">โดยทั่วไป จะถูกโฮสต์ในระบบการจัดการเนื้อหา เครือข่ายส่งเนื้อหา (CDN) หรือเซิร์ฟเวอร์สื่อ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>MPOS then fetches and displays the images for the appropriate entities, such as products and catalogs, by accessing the target URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากนั้น MPOS นำมาใช้และแสดงรูปภาพสำหรับเอนทิตี้ที่เหมาะสม เช่น ผลิตภัณฑ์และแค็ตตาล็อก โดนการเข้าถึง URL เป้าหมาย</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To fetch these externally hosted images, MPOS requires the correct URL format for the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อที่จะนำรูปภาพที่ถูกโฮสต์จากภายนอกเหล่านี้มาใช้ MPOS จำเป็นต้องมีรูปแบบ URL ที่ถูกต้องสำหรับรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can configure the required URL format for the images by setting up the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> value in the channel profile and using the <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> functionality for each entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถตั้งค่าคอนฟิกรูปแบบ URL ที่จำเป็นสำหรับรูปภาพโดยการตั้งค่าค่า <bpt id="p1">**</bpt>URL ฐานสื่อ<ept id="p1">**</ept>ในโพรไฟล์ช่องและใช้ฟังก์ชัน <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept>สำหรับแต่ละเอนทิตี้ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also overwrite the standard URL format for a subset of entities by using the <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept> functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถบันทึกทับรูปแบบ URL มาตรฐานสำหรับชุดย่อยของเอนทิตี โดยการใช้ฟังก์ชั่น <bpt id="p1">**</bpt>แก้ไขใน Excel<ept id="p1">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the current version of Dynamics 365 for Retail, you can no longer set up the URL format by using the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute XML for MPOS in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในรุ่นปัจจุบันของ Dynamics 365 for Retail คุณไม่สามารถตั้งค่ารูปแบบ URL โดยการใช้ XML แอททริบิวต์ <bpt id="p1">**</bpt>รูปภาพ<ept id="p1">**</ept> สำหรับ MPOS ในกลุ่มแอททริบิวต์ <bpt id="p2">**</bpt>เริ่มต้น<ept id="p2">**</ept> สำหรับเอนทิตี้ได้อีกต่อไป</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If you're familiar with Microsoft Dynamics AX 2012 R3 and are now using the current version of Dynamics 365 for Retail, make sure that you always use the new <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality to set up images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้าคุณคุ้นเคยกับ Microsoft Dynamics AX 2012 R3 และขณะนี้กำลังใช้รุ่นปัจจุบันของ Dynamics 365 for Retail กรุณาตรวจสอบให้แน่ใจว่า คุณใช้ฟังก์ชัน <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> ใหม่เสมอเพื่อตั้งค่ารูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Don't use or modify the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for any entities, including products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่าใช้หรือปรับเปลี่ยนแอททริบิวต์ <bpt id="p1">**</bpt>รูปภาพ<ept id="p1">**</ept> ในกลุ่มแอททิรบิวต์ <bpt id="p2">**</bpt>เริ่มต้น<ept id="p2">**</ept> สำหรับเอนทิตีใด ๆ รวมถึงผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Changes that you make directly in the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> attribute group for images won't be reflected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การเปลี่ยนแปลงที่คุณทำได้โดยตรงในกลุ่มแอททริบิวต์ <bpt id="p1">**</bpt>เริ่มต้น<ept id="p1">**</ept> สำหรับรูปภาพจะไม่สะท้อนให้เห็น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This option will be disabled in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวเลือกนี้จะไม่ทำงานในรุ่นต่อไป</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the following procedures, images are set up for the Catalog entity as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกระบวนงานต่อไปนี้ รูปภาพจะถูกตั้งค่าสำหรับเอนทิตี้แค็ตตาล็อกเป็นตัวอย่าง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These procedures will help guarantee that the correct image destination path is set implicitly for all catalog images that use a common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กระบวนงานเหล่านี้จะช่วยรับประกันว่า เส้นทางปลายทางของรูปภาพที่ถูกต้องถูกตั้งค่าสำหรับรูปภาพแค็ตตาล็อกทั้งหมดที่ใช้เส้นทางทั่วไปโดยนัย</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, if you've set up a media server or CDN externally, and want the images to appear in MPOS for a given store, the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality helps you the set the path where MPOS can look up and retrieve the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น ถ้าคุณได้ตั้งค่าเซิร์ฟเวอร์สื่อหรือ CDN จากภายนอก และต้องการให้รูปภาพปรากฏใน MPOS สำหรับร้านค้าที่กำหนด ฟังก์ชัน <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> จะช่วยคุณตั้งเส้นทางที่ MPOS สามารถค้นหาและดึงข้อมูลรูปภาพได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For this demo data example, the media server is deployed on the Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับตัวอย่างข้อมูลสาธิตนี้ เซิร์ฟเวอร์สื่อถูกปรับใช้บนเซิร์ฟเวอร์ Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, you can have it anywhere outside Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม คุณสามารถใช้ที่ใดก็ได้ภายนอก Dynamics 365 for Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Set up the media base URL for a channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่า URL ฐานสื่อสำหรับช่องทาง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the Dynamics 365 for Retail HQ portal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เปิดพอร์ทัล Dynamics 365 for Retail HQ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel profiles<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ตั้งค่าช่องทาง<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>โพรไฟล์ช่องทาง<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigation<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>การนำทาง<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the channel profile that your store uses for MPOS, update the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> field with the base URL of your media server or CDN.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ในโพรไฟล์ช่องทางที่ร้านค้าของคุณใช้สำหรับ MPOS อัพเดตฟิลด์ <bpt id="p1">**</bpt>URL ฐานสื่อ<ept id="p1">**</ept> ด้วย URL ฐานสื่อของเซิร์ฟเวอร์สื่อหรือ CDN ของคุณ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The base URL is the first part of the URL that is shared by all image folders of different entities.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ฐาน URL คือ ส่วนแรกของ URL ที่ถูกใช้ร่วมกันโดยโฟลเดอร์รูปภาพทั้งหมดของเอนทิตี้ที่แตกต่างกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Channel profiles page<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>หน้าโพรไฟล์ช่องทาง<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Define the media template for an entity</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">กำหนดเท็มเพลตสื่อสำหรับเอนทิตี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>การจัดการแค็ตตาล็อก<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, on the Action Pane, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในหน้า <bpt id="p1">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p1">**</ept> บนบานหน้าต่างการดำเนินการ คลิก <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกล่องโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> ในฟิลด์ <bpt id="p2">**</bpt>เอนทิตี้<ept id="p2">**</ept> <bpt id="p3">**</bpt>แค็ตตาล็อก<ept id="p3">**</ept> ควรถูกเลือกตามค่าเริ่มต้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, enter the remaining path of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในแท็บด่วน <bpt id="p1">**</bpt>เส้นทางสื่อ<ept id="p1">**</ept> ป้อนเส้นที่เหลืออยู่ของสถานที่เก็บรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The media path supports <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> as a variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เส้นทางสื่อสนับสนุน <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> เป็นตัวแปร</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, for the demo data, you can create a <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> folder for all catalog images under the media base URL for your media server (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น สำหรับข้อมูลสาธิต คุณสามารถสร้างโฟลเดอร์ <bpt id="p1">**</bpt>แค็ตตาล็อก<ept id="p1">**</ept> สำหรับรูปภาพแค็ตตาล็อกทั้งหมด ภายใต้ URL ฐานสื่อสำหรับเซิร์ฟเวอร์สื่อของคุณ (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can then have a folder for each language, such as en-US or fr-FR, and copy the appropriate images under each folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากนั้นคุณสามารถมีโฟลเดอร์สำหรับแต่ละภาษา เช่น อังกฤษ-สหรัฐอเมริกา หรือ ฝรั่งเศส-ฝรั่งเศส และคัดลอกรูปภาพที่เหมาะสมภายใต้แต่ละโฟลเดอร์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have different images for the various languages, you can omit the <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> variable from your folder structure and point directly to the Catalogs folder that contains the catalog images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้าคุณไม่มีรูปภาพที่แตกต่างกันสำหรับภาษาต่าง ๆ คุณสามารถข้ามตัวแปร <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> จากโครงสร้างโฟลเดอร์ของคุณและมุ่งโดยตรงไปยังโฟลเดอร์แค็ตตาล็อกที่ประกอบด้วยรูปภาพแค็ตตาล็อกได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The current version of Dynamics 365 for Retail supports the <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> token for Catalog, Product, and Category entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รุ่นปัจจุบันของ Dynamics 365 for Retail สนับสนุนโทเคน <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> สำหรับเอนทิตี้แค็ตตาล็อก ผลิตภัณฑ์ และประเภท</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>(The <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> token isn't supported for Customer and Worker entities, according to the existing standard that has been effective since Microsoft Dynamics AX 6.x.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(โทเคน <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> ไม่ได้รับการสนับสนุนสำหรับเอนทิตีลูกค้าและผู้ปฏิบัติงาน ตามมาตรฐานที่มีอยู่ที่มีการมีผลบังคับใช้นับตั้งแต่ Microsoft Dynamics AX 6.x.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For images, the file name format is hard-coded to the catalog name and can't be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับรูปภาพ รูปแบบชื่อไฟล์ตายตัวกับชื่อแค็ตตาล็อกและไม่สามารถถูกเปลี่ยนแปลงได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Therefore, rename your images so that they have appropriate catalog names, to help guarantee that MPOS handles them correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดังนั้น เปลี่ยนชื่อรูปภาพของคุณเพื่อให้มีชื่อแค็ตตาล็อกที่เหมาะสม เพื่อที่จะช่วยรับประกันว่า MPOS จัดการได้อย่างถูกต้อง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>File Extension<ept id="p1">**</ept> field, select the expected file name extension, depending on the type of images that you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในฟิลด์ <bpt id="p1">**</bpt>นามสกุลไฟล์<ept id="p1">**</ept> เลือกนามสกุลไฟล์ที่คาดไว้ โดยขึ้นอยู่กับชนิดของรูปภาพที่คุณมี</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example, for the demo data, the catalog images are set to the .jpg extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น สำหรับข้อมูลสาธิต รูปภาพแค็ตตาล็อกจะถูกกำหนดเป็นนามสกุล .jpg</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>(The image files are also renamed so that they have catalog names.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ไฟล์รูปภาพจะถูกเปลี่ยนชื่อเพื่อให้มีชื่อแค็ตตาล็อกด้วยเช่นกัน)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To validate that the media template for images has been saved correctly, on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อตรวจสอบว่าเท็มเพลตสื่อสำหรับรูปภาพถูกบันทึกอย่างถูกต้อง ในหน้า <bpt id="p1">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p1">**</ept> คลิก <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept> อีกครั้ง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To validate the template without closing the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, you can use the <bpt id="p2">**</bpt>Generate Image URLs for Excel<ept id="p2">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อตรวจสอบเท็มเพลตโดยไม่มีการปิดกล่องโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> คุณสามารถใช้แท็บด่วน <bpt id="p2">**</bpt>สร้าง URL ของรูปภาพสำหรับ Excel<ept id="p2">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Check the appearance of the image URL, and verify that the URL complies with the template standard that was mentioned earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เช็คลักษณะของ URL ของรูปภาพ และตรวจสอบว่า URL นั้นสอดคล้องกับมาตรฐานเท็มเพลตที่ถูกกล่าวถึงก่อนหน้านี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box has now set the image path implicitly for all catalog images that use this common URL path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กล่องโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> ขณะนี้ได้ตั้งเส้นทางโดยนัยสำหรับรูปภาพแค็ตตาล็อกทั้งหมดที่ใช้เส้นทาง URL ทั่วไปนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This URL path applies to all catalog images unless they are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เส้นทาง URL นี้ใช้กับรูปภาพแค็ตตาล็อกทั้งหมดยกเว้นว่าถูกบันทึกทับ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The first part of the image path is taken from the media base URL that you defined in the channel profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนแรกของเส้นทางรูปภาพจะถูกนำมาจาก URL ฐานสื่อที่คุณกำหนดไว้ในโพรไฟล์ช่องทาง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The remaining part of the path is taken from the path that you defined in the media template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนที่เหลือของเส้นทางจะถูกนำมาจากเส้นทางที่คุณกำหนดไว้ในเท็มเพลตสื่อ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The two parts are concatenated to provide the full URL of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทั้งสองส่วนจะถูกเรียงต่อกันเพื่อจัดเตรียม URL แบบเต็มของสถานที่เก็บรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For example, a catalog in the demo data is named Fabrikam Base Catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น แค็ตตาล็อกในข้อมูลสาธิตที่ถูกตั้งชื่อแค็ตตาล็อกฐานของ Fabrikam</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Therefore, the image name must be Fabrikam Base Catalog.jpg so that it uses the catalog name and the .jpg file name extension that is configured in the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดังนั้น ชื่อรูปภาพต้องมี Fabrikam Base Catalog.jpg เพื่อให้ใช้ชื่อแค็ตตาล็อกและนามสกุลไฟล์ .jpg ที่ถูกตั้งค่าคอนฟิกในเท็มเพลต</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In this case, after concatenation, the URL will be <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกรณีนี้ หลังจากการเรียงต่อกัน URL จะเป็น <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Run the synchronization jobs to push the new template to the channel database, so that MPOS can use the template to access the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รันงานการซิงโครไนส์เพื่อที่จะกำหนดเท็มเพลตใหม่ไปยังฐานข้อมูลช่องทาง เพื่อให้ MPOS สามารถใช้เท็มเพลตนั้นในการเข้าถึงรูปภาพได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To update the media template for catalog images on the channel side, be sure to run <bpt id="p1">**</bpt>Catalog Job 1150<ept id="p1">**</ept> from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เพื่อที่จะอัพเดตเท็มเพลตสื่อสำหรับรูปภาพแค็ตตาล็อกในฝั่งช่องทาง ให้แน่ใจว่าได้รัน <bpt id="p1">**</bpt>งานแค็ตตาล็อก 1150<ept id="p1">**</ept> จาก <bpt id="p2">**</bpt>ฝ่ายไอทีระบบขายปลีก<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>กำหนดการการจัดจำหน่าย<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>กำหนดกล่องโต้ตอบเท็มเพลตของสื่อ<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Previewing an image from the entity level</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">แสดงตัวอย่างรูปภาพจากระดับเอนทิตี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>From the page for the entity item in HQ, you can preview the image that uses the image URL that is derived from the media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">จากหน้าสำหรับสินค้าเอนทิตี้แบบ HQ คุณสามารถแสดงตัวอย่าง URL รูปภาพที่ถูกส่งมาจากเท็มเพลตสื่อ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For this example, go to the appropriate catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับตัวอย่างนี้ ไปยังแค็ตตาล็อกที่เหมาะสม และจากนั้น บนบานหน้าต่างการดำเนินการ คลิก <bpt id="p1">**</bpt>สื่อ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>&gt; รูปภาพ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Use the drop-down list to select different stores that might have different channel profiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ใช้รายการแบบหล่นลงเพื่อเลือกร้านค้าต่าง ๆ ที่อาจมีโพรไฟล์ช่องทางที่แตกต่างกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To edit or remove the implicit media template, you must return to the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box for the <bpt id="p2">**</bpt>Catalog images<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อแก้ไขหรือลบเท็มเพลตสื่อโดยนัย คุณต้องส่งคืนไปยังกล่องโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> สำหรับหน้า <bpt id="p2">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can use the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept> buttons to manually change the path that is based on the implicit template and used for a specific image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถใช้ปุ่ม <bpt id="p1">**</bpt>เพิ่ม<ept id="p1">**</ept> และ <bpt id="p2">**</bpt>ลบ<ept id="p2">**</ept> เพื่อที่จะเปลี่ยนเส้นทางที่ยึดตามเท็มเพลตโดยนัย และใช้สำหรับรูปภาพเฉพาะ ด้วยตนเองได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For more information, see the <bpt id="p1">[</bpt>Overwriting the media template for entity items<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> section later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับข้อมูลเพิ่มเติม ดูส่วน <bpt id="p1">[</bpt>บันทึกทับสื่อเท็มเพลตสำหรับรายการเอนทิตี<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> ภายหลังในบทความนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>After you've finished previewing an image and making any changes that you require, start the MPOS instance for the appropriate store, and see whether the catalog images are shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">หลังจากที่คุณได้เสร็จสิ้นการแสดงตัวอย่างรูปภาพ และทำการเปลี่ยนแปลงใด ๆ ที่คุณต้องการ เริ่มต้นอินสแตนซ์ MPOS สำหรับร้านค้าที่เหมาะสม และดูว่ารูปภาพแค็ตตาล็อกถูกแสดงหรือไม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Images dialog box<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>กล่องโต้ตอบภาพ<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use the same procedure for all the five entities that are supported: Worker, Customer, Catalog, Category, and Products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คุณสามารถใช้กระบวนงานเดียวกันสำหรับเอนทิตีทั้งหมดห้ารายการที่ได้รับการสนับสนุน: ผู้ปฏิบัติงาน ลูกค้า แค็ตตาล็อก ประเภท และผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>"Catalog Products" (products that are set at the catalog level) and "Channel Products" (products that are set at the channel level) use the media template that is set for the Products entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"แค็ตตาล็อกผลิตภัณฑ์" (ผลิตภัณฑ์ที่ถูกตั้งค่าไว้ในระดับแค็ตตาล็อก) และ "ผลิตภัณฑ์ตามช่องทาง" (ผลิตภัณฑ์ที่ถูกตั้งค่าในระดับช่องทาง) ใช้เท็มเพลตสื่อที่ถูกตั้งค่าสำหรับเอนทิตี้ผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For the Products media template, you can select the number of product images to show per product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับเท็มเพลตสื่อผลิตภัณฑ์ คุณสามารถเลือกหมายเลขของรูปภาพผลิตภัณฑ์เพื่อแสดงแต่ละผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can also set the default image for a given product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณยังสามารถกำหนดรูปภาพเริ่มต้นสำหรับผลิตภัณฑ์ที่ระบุได้ด้วยเช่นกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In this way, you can prevent blank images in MPOS and help to control which image is used as the default image for a product item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ด้วยวิธีนี้ คุณสามารถป้องกันไม่ให้มีรูปภาพที่ว่างเปล่าใน MPOS และช่วยควบคุมว่ารูปภาพใดจะถูกใช้เป็นรูปภาพเริ่มต้นสำหรับผลิตภัณฑ์หนึ่ง ๆ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the following example, each product has five images, and the first image is set as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตัวอย่างต่อไปนี้ แต่ละผลิตภัณฑ์มีรูปภาพห้ารูป และรูปภาพแรกถูกตั้งเป็นรูปภาพเริ่มต้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Variant products are treated the same way as master products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์ย่อยจะถูกปฏิบัติในลักษณะเดียวกันกับผลิตภัณฑ์หลัก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The file name of the image file should be based on the product number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ชื่อไฟล์ของไฟล์รูปภาพควรจะขึ้นอยู่กับหมายเลขผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Some characters are also escaped while the file name is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อักขระบางตัวจะหายไปขณะที่มีสร้างชื่อไฟล์ด้วยเช่นกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, it's a good to verify the file name by using the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ดังนั้น จึงเป็นการดีที่จะตรวจสอบชื่อไฟล์ โดยการใช้ส่วน <bpt id="p1">**</bpt>สร้าง URL ของรูปภาพสำหรับ Excel<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>กำหนดกล่องโต้ตอบเท็มเพลตของสื่อ<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Synchronization jobs to send a media template to the channel side</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">งานการซิงโครไนส์เพื่อส่งเท็มเพลตสื่อไปยังด้านช่องทาง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For all the five supported entities (Worker, Customer, Catalog, Category, and Products), whenever you update the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog to set up an image, make sure that you run the Catalog job (1150) from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทั้งหมดห้าเอนทิตี้ที่ถูกสนับสนุน (ผู้ปฏิบัติงาน ลูกค้า แค็ตตาล็อก ประเภท และผลิตภัณฑ์) เมื่อใดก็ตามที่คุณอัพเดตการโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> เพื่อตั้งค่ารูปภาพ ตรวจสอบให้แน่ใจว่าคุณรันงานแค็ตตาล็อก (1150) จาก <bpt id="p2">**</bpt>ไอทีขายปลีก<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>กำหนดการการจัดจำหน่าย<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This job will enable the updated media template to be synced to the channel and used by MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">งานนี้จะเปิดใช้งานเท็มเพลตสื่อที่อัพเดตแล้วเพื่อที่จะซิงค์ไปยังช่องทาง และถูกใช้โดย MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Run the Catalog job (1150) after you make any of the following changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รันงานแค็ตตาล็อก (1150) หลังจากที่คุณทำการเปลี่ยนแปลงใด ๆ ต่อไปนี้:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>You update the Catalog image media template from <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณอัพเดตเท็มเพลตสื่อรูปภาพแค็ตตาล็อกจาก <bpt id="p1">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You update the Employee image media template from <bpt id="p1">**</bpt>Employee images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณอัพเดตเท็มเพลตสื่อรูปภาพพนักงานจาก <bpt id="p1">**</bpt>รูปภาพพนักงาน<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>You update the Customer image media template from <bpt id="p1">**</bpt>Customer image<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณอัพเดตเท็มเพลตสื่อรูปภาพลูกค้าจาก <bpt id="p1">**</bpt>รูปภาพลูกค้า<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You update the Product image media template from <bpt id="p1">**</bpt>Product images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณอัพเดตเท็มเพลตสื่อรูปภาพผลิตภัณฑ์จาก <bpt id="p1">**</bpt>รูปภาพผลิตภัณฑ์<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You update the Category image media template from <bpt id="p1">**</bpt>Category images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณอัพเดตเท็มเพลตสื่อรูปภาพของประเภทจาก <bpt id="p1">**</bpt>รูปภาพของประเภท<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You must also publish the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณยังต้องเผยแพร่ช่องทางด้วยเช่นกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Overwriting the media template for entity items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การบันทึกทับเท็มเพลตสื่อสำหรับเอนทิตี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>As you learned in the previous section, the media template for a given entity supports only one common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตามที่คุณได้เรียนรู้ในส่วนก่อนหน้านี้ เท็มเพลตสื่อสำหรับเอนทิตีที่กำหนดสนับสนุนเพียงหนึ่งเส้นทางทั่วไป</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>This path is based on the media base URL that is configured and the media path that is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เส้นทางนี้จะขึ้นอยู่กับ URL ฐานสื่อที่ถูกตั้งค่าคอนฟิกและเส้นทางสื่อที่ถูกกำหนดไว้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>However, in many cases, a retailer wants to be able to use images from different sources for a subset of items in an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม ในหลายกรณี ผู้ค้าปลีกต้องการให้สามารถใช้รูปภาพจากแหล่งข้อมูลที่แตกต่างกันสำหรับชุดย่อยของสินค้าในเอนทิตี้ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, a store uses the self-hosted media server for one set of catalog images but uses CDN URLs for another set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น ร้านค้าใช้เซิร์ฟเวอร์สื่อที่ตนเองเป็นโฮสต์สำหรับชุดของรูปภาพแค็ตตาล็อก แต่ใช้ URL ของ CDN สำหรับชุดอื่น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To overwrite image URLs that are based on a media template for entity images at the entity level, you can use the Edit in Excel and Manual edit functionality from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อที่จะบันทึกทับ URL ของรูปภาพที่ขึ้นอยู่กับเท็มเพลตสื่อสำหรับรูปภาพเอนทิตี้ที่ระดับเอนทิตี้ คุณสามารถใช้การแก้ไขใน Excel และฟังก์ชันแก้ไขด้วยตนเอง จากหน้า <bpt id="p1">**</bpt>แสดงตัวอย่าง<ept id="p1">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Overwrite by using Edit in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เขียนทับโดยการแก้ไขใน Excel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>การจัดการแค็ตตาล็อก<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในหน้า <bpt id="p1">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p1">**</ept> คลิก <bpt id="p2">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกล่องโต้ตอบ <bpt id="p1">**</bpt>กำหนดเท็มเพลตสื่อ<ept id="p1">**</ept> ในฟิลด์ <bpt id="p2">**</bpt>เอนทิตี้<ept id="p2">**</ept> <bpt id="p3">**</bpt>แค็ตตาล็อก<ept id="p3">**</ept> ควรถูกเลือก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, notice the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในแท็บด่วน <bpt id="p1">**</bpt>เส้นทางสื่อ<ept id="p1">**</ept> สังเกตสถานที่เก็บรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>On the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Generate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในแท็บด่วน <bpt id="p1">**</bpt>สร้าง URL ของรูปภาพสำหรับ Excel<ept id="p1">**</ept> คลิก <bpt id="p2">**</bpt>สร้าง<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Whenever the media template is changed, you must click <bpt id="p1">**</bpt>Generate<ept id="p1">**</ept> before you can use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ทุกครั้งที่เท็มเพลตสื่อถูกเปลี่ยนแปลง คุณต้องคลิก <bpt id="p1">**</bpt>สร้าง<ept id="p1">**</ept> ก่อนที่คุณจะสามารถใช้ฟังก์ชันแก้ไขใน Excel ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>สร้าง URL รูปภาพสำหรับ FastTab ของ Excel<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You now see a preview of the image URLs that were generated based on the last saved media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ขณะนี้คุณจะเห็นการแสดงตัวอย่างของรูปภาพ URL ที่ถูกสร้างขึ้นตามเท็มเพลตสื่อที่ถูกบันทึกไว้ล่าสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab after Generate is selected<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>สร้าง URL รูปภาพสำหรับ FastTab ของ Excel หลังจากการเลือก สร้าง<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The URLs that are generated for Excel use the path and conventions of the media template that is defined.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">URL ที่ถูกสร้างขึ้นสำหรับ Excel ใช้เส้นทางและแบบแผนของเท็มเพลตสื่อที่ถูกกำหนดไว้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These conventions include the conventions for file names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แบบแผนเหล่านี้รวมถึงข้อตกลงสำหรับชื่อไฟล์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The expectation is that you've set up the physical images outside Dynamics 365 for Retail, and the images can be retrieved from the URLs that are derived from the media template that you defined earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สิ่งที่คาดหวังคือคุณได้ตั้งค่ารูปภาพทางกายภาพที่มีอยู่จริงนอก Dynamics 365 for Retail และรูปภาพสามารถถูกดึงข้อมูลจาก URL ที่ถูกส่งมาจากเท็มเพลตสื่อที่คุณได้กำหนดไว้ก่อนหน้านี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can overwrite these derived URLs by using the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถบันทึกทับ URL ที่ได้รับโดยการใช้ฟังก์ชันแก้ไขใน Excel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Click <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>แก้ไขใน Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>After the Microsoft Excel worksheet is opened, click <bpt id="p1">**</bpt>Enable edit<ept id="p1">**</ept> when you're prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากที่มีการเปิดแผ่นงาน Microsoft Excel คลิก <bpt id="p1">**</bpt>เปิดใช้งานการแก้ไข<ept id="p1">**</ept> เมื่อคุณได้รับพร้อมท์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>When you're prompted, click <bpt id="p1">**</bpt>Trust this add-in<ept id="p1">**</ept> in the right pane, and wait for the add-in to complete the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อคุณได้รับพร้อม คลิก <bpt id="p1">**</bpt>เชื่อถือ add-in นี้<ept id="p1">**</ept> ในบานหน้าต่างด้านขวา และรอให้ add-in นี้ทำการติดตั้งให้เสร็จสมบูรณ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trust this add-in<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>เชื่อถือ Add-in นี้<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you're prompted to sign in, enter the credentials that you used to sign in to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้าคุณพร้อมที่จะลงชื่อเข้าใช้ ป้อนข้อมูลประจำตัวที่คุณใช้ในการลงชื่อเข้า HQ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sign-in prompt<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ความพร้อมในการลงชื่อเข้าใช้<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>After you sign in, you should be able to see the list of image URLs for the various catalog entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากที่คุณลงชื่อเข้าใช้ คุณควรจะสามารถดูรายการของ URL ของรูปภาพสำหรับรายการต่าง ๆ ในแค็ตตาล็อกได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>You edit, add, and remove the image URLs for various entity items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณแก้ไข เพิ่ม และลบ URL ของรูปภาพสำหรับสินค้าต่าง ๆ ของเอนทิตี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>For all entities except Products, you can overwrite the image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับเอนทิตี้ทั้งหมดยกเว้นผลิตภัณฑ์ คุณสามารถบันทึกทับ URL ของรูปภาพได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Modify the existing image URL, so that it uses the new destination URL of the image, and update the file name with the new file name for the image file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แก้ไข URL รูปภาพที่มีอยู่ เพื่อให้ใช้ URL ปลายทางใหม่ของรูปภาพ และอัพเดตชื่อไฟล์ด้วยชื่อไฟล์ใหม่สำหรับไฟล์รูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The file name must be unique to help guarantee that the record is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ชื่อไฟล์ต้องไม่ซ้ำกันเพื่อช่วยในการรับประกันว่าเรกคอร์ดไม่ซ้ำกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Overwrite the image URLs in Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>บันทึกทับ URL ของรูปภาพใน Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>When you overwrite image URLs for Products entities by using the Edit in Excel functionality or the entity item page, MPOS always shows all the media template image URLs together with the overwritten image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อคุณบันทึกทับ URL ของรูปภาพสำหรับเอนทิตีผลิตภัณฑ์ โดยการใช้ฟังก์ชันแก้ไขใน Excel หรือหน้าสินค้าเอนทิตี MPOS จะแสดง URL ของรูปภาพเท็มเพลตสื่อทั้งหมดร่วมกับ URL ของรูปภาพที่ถูกบันทึกทับ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>After you've finished making your changes, click <bpt id="p1">**</bpt>Publish in Excel<ept id="p1">**</ept> to create a new explicit association entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากที่คุณเสร็จสิ้นการทำการเปลี่ยนแปลงของคุณ คลิก <bpt id="p1">**</bpt>เผยแพร่ใน Excel<ept id="p1">**</ept> เพื่อสร้างการเชื่อมโยงที่ชัดเจนรายการใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Return to HQ, and click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กลับไปยัง HQ และคลิก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Run the appropriate synchronization jobs for the entity, and check the preview on the entity page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รันงานการซิงโครไนส์ที่เหมาะสมสำหรับเอนทิตี้ และเช็คการแสดงตัวอย่างบนหน้าเอนทิตี้หรือใน MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Creating new records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การสร้างเรกคอร์ดใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>You can create new records in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถสร้างเรกคอร์ดใหม่ได้ใน Excel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>However, make sure that you provide the correct information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม ตรวจสอบให้แน่ใจว่าคุณจัดเตรียมข้อมูลที่ถูกต้องไว้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>For example, to create a new entry for a catalog, make sure that the catalog ID and catalog name are correct, and also provide a unique file name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น เพื่อสร้างรายการใหม่สำหรับแค็ตตาล็อก ตรวจสอบให้แน่ใจว่ารหัสแค็ตตาล็อกและชื่อแค็ตตาล็อกถูกต้อง และจัดเตรียมให้ชื่อไฟล์ไม่ซ้ำกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The unique file name is very important, because the uniqueness of records in Excel is validated during publishing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ชื่อไฟล์ที่ไม่ซ้ำกันมีความสำคัญมาก เนื่องจากการไม่ซ้ำกันของเรกคอร์ดใน Excel จะผ่านการตรวจสอบในระหว่างการเผยแพร่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>First copy the details from the catalog that you want to create a new record for, and copy the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อันดับแรก คัดลอกรายละเอียดจากแค็ตตาล็อกที่คุณต้องการสร้างเรกคอร์ดใหม่ และคัดลอกเรกคอร์ด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You just have to update the file name and URL, because the rest of the information will be same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณเพียงต้องอัพเดตชื่อไฟล์และ URL เนื่องจากข้อมูลที่เหลือจะเป็นแบบเดียวกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To create new records for Product entity items, you use the same basic procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อสร้างเรกคอร์ดใหม่สำหรับสินค้าเอนทิตี้ผลิตภัณฑ์ คุณต้องใช้กระบวนงานพื้นฐานเดียวกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>From the Excel worksheet, copy an existing record for the product that you to create a new record for, and then replace the image URL and filename.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากแผ่นงาน Excel คัดลอกเรกคอร์ดที่มีอยู่แล้วสำหรับผลิตภัณฑ์ที่คุณจะสร้างเรกคอร์ดใหม่ และจากนั้นแทนที่ URL ของรูปภาพและชื่อไฟล์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Make sure that the file name is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตรวจสอบให้แน่ใจว่าชื่อแฟ้มไม่ซ้ำกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Deleting an existing record</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การลบเรกคอร์ดที่มีอยู่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Only the overwritten image URL records can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เฉพาะเรกคอร์ด URL ของรูปภาพที่ถูกบันทึกทับเท่านั้นที่ถูกลบได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>After an image is deleted and synchronization is completed, the image will no longer appear on the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากที่รูปภาพถูกลบ และการซิงโครไนส์เสร็จสมบูรณ์ รูปภาพจะไม่ปรากฏในหน้า <bpt id="p1">**</bpt>แสดงตัวอย่าง<ept id="p1">**</ept> หรือใน MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Image URL records that are derived from the media template can't be deleted, because these records are always derived from the media template every time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เรกคอร์ด URL ของรูปภาพที่ถูกส่งมาจากเท็มเพลสื่อไม่สามารถถูกลบได้ เนื่องจากเรกคอร์ดเหล่านี้ถูกส่งมาจากเท็มเพลตสื่อเสมอทุกครั้ง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Overwrite from the entity-level Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บันทึกทับจากหน้าแสดงตัวอย่างระดับเอนทิตี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>For all entities except Products, you can overwrite the image URL for a given entity item at the entity item level from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับเอนทิตีทั้งหมดยกเว้นผลิตภัณฑ์ คุณสามารถบันทึกทับ URL ของรูปภาพสำหรับเอนทิตี้ที่ระบุสินค้าที่ระดับสินค้าเอนทิตี้จากหน้า <bpt id="p1">**</bpt>แสดงตัวอย่าง<ept id="p1">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>For Products, you can use the "Catalog Products" entity page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับผลิตภัณฑ์ คุณสามารถใช้หน้าเอนทิตี้ "ผลิตภัณฑ์แค็ตตาล็อก"</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This example shows how to overwrite a catalog image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างนี้แสดงวิธีการบันทึกทับรูปภาพแค็ตตาล็อก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Click <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Media<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Images<ept id="p3">**</ept>, and select the catalog image to update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>แค็ตตาล็อก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>สื่อ<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>รูปภาพ<ept id="p3">**</ept> และเลือกรูปภาพแค็ตตาล็อกเพื่ออัพเดต</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and enter the image URL to overwrite the media template URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>เพิ่ม<ept id="p1">**</ept> และป้อน URL ของรูปภาพเพื่อบันทึกทับ URL เท็มเพลตสื่อ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you want this image to be shown in MPOS for the catalog, you can set it as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้าคุณต้องการให้รูปภาพนี้ถูกแสดงใน MPOS สำหรับแค็ตตาล็อก คุณสามารถตั้งเป็นรูปภาพเริ่มต้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept> ระบบจะนำเข้าข้อมูลการชำระเงิน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The image URL is updated for this catalog image, and a preview is shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">URL ของรูปภาพมีถูกอัพเดตสำหรับรูปภาพแค็ตตาล็อกนี้ และการแสดงตัวอย่างจะถูกแสดงขึ้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>URL updated in the New image dialog box<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>URL ที่ปรับปรุงในกล่องโต้ตอบรูปภาพใหม่<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can also see the image preview for all overwritten image URLs on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> gallery page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คุณยังสามารถดูตัวอย่างรูปภาพสำหรับ URL รูปภาพที่ถูกบันทึกทับทั้งหมดในหน้าแกลเลอรี <bpt id="p1">**</bpt>รูปภาพแค็ตตาล็อก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Catalog images gallery page<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>หน้าแกลเลอรีรูปภาพในแค็ตตาล็อก<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Currently, the gallery doesn't show image previews for media template image URLs.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ในปัจจุบัน แกลเลอรีไม่แสดงตัวอย่างรูปภาพสำหรับ URL ของรูปภาพเท็มเพลตสื่อ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>For Catalog, Worker, Customer, and Category entities, if the user explicitly provides a URL through this page, we recommend that you indicate which image is the default image, because Retail Server clients show only one image per Catalog, Customer, Worker, and Category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับเอนทิตี้แค็ตตาล็อก ผู้ปฏิบัติงาน ลูกค้า และประเภท ถ้าผู้ใช้จัดเตรียม URL อย่างชัดเจนผ่านหน้านี้ เราขอแนะนำให้คุณระบุรูปภาพที่เป็นรูปภาพเริ่มต้น เนื่องจากลูกค้าเซิร์ฟเวอร์ขายปลีกแสดงรูปภาพเดียวเท่านั้นต่อแค็ตตาล็อก ลูกค้า ผู้ปฏิบัติงาน และประเภท</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If the user doesn't specify a default image, the system determines the default image and send it to the Retail service caller (MPOS or Ecommerce).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้าผู้ใช้ไม่ได้ระบุรูปภาพเริ่มต้น ระบบจะกำหนดรูปภาพเริ่มต้นและส่งไปยังผู้เรียกบริการขายปลีก (MPOS หรือ Ecommerce)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Overwrite the image URL for catalog product images from the Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บันทึกทับ URL ของรูปภาพสำหรับรูปภาพผลิตภัณฑ์แค็ตตาล็อกจากหน้าแสดงตัวอย่าง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>To overwrite image URLs for catalog product images, you must use the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อที่จะบันทึกทับ URL ของรูปภาพสำหรับรูปภาพผลิตภัณฑ์แค็ตตาล็อก คุณต้องใช้หน้า <bpt id="p1">**</bpt>แสดงตัวอย่าง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You can't use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณไม่สามารถใช้ฟังก์ชันแก้ไขใน Excel ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>To overwrite product images at a catalog level, select a catalog, and then select the product to overwrite the image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อที่จะบันทึกทับรูปภาพผลิตภัณฑ์ที่ระดับแค็ตตาล็อก เลือกแค็ตตาล็อก และจากนั้นเลือกผลิตภัณฑ์เพื่อบันทึกทับรูปภาพ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Click <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>แอททริบิวต์<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>On the next page, select <bpt id="p1">**</bpt>Image<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในหน้าถัดไป เลือก <bpt id="p1">**</bpt>รูปภาพ<ept id="p1">**</ept> และจากนั้น คลิก <bpt id="p2">**</bpt>แก้ไข<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page opens as a slider dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หน้า <bpt id="p1">**</bpt>แสดงตัวอย่าง<ept id="p1">**</ept> เปิดเป็นกล่องโต้ตอบแบบเลื่อน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and overwrite the image URL with a new URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>เพิ่ม<ept id="p1">**</ept> และบันทึกทับ URL ของรูปภาพด้วย URL ใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>ตกลง<ept id="p1">**</ept> ระบบจะนำเข้าข้อมูลการชำระเงิน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>You now see the preview of the new image and can set it as the default image.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ขณะนี้คุณจะเห็นการแสดงตัวอย่างรูปภาพใหม่ และสามารถตั้งค่าเป็นรูปภาพเริ่มต้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Image preview in the New image dialog box<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>การแสดงตัวอย่างรูปภาพในกล่องโต้ตอบรูปภาพใหม่<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>After category image association, you must publish the channel and run the Channel job to help guarantee that the changes are published to the channel database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">หลังจากการเชื่อมโยงรูปภาพประเภท คุณต้องเผยแพร่ช่องทางและช่องทางที่จะช่วยรับประกันว่า การเปลี่ยนแปลงถูกเผยแพร่ไปยังฐานข้อมูลช่องทาง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Setting up images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การตั้งค่ารูปภาพผลิตภัณฑ์เพื่อที่จะแสดงอยู่ในโหมดออฟไลน์สำหรับ MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>MPOS can run in Online mode (when MPOS connected to Retail Server) or Offline mode (when there is no Retail Server or network connectivity, and transactions are stored in a local offline database).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS สามารถรันในโหมดออนไลน์ (เมื่อ MPOS เชื่อมต่อกับเซิร์ฟเวอร์ขายปลีก) หรือโหมดออฟไลน์ (เมื่อไม่มีการเชื่อมต่อเซิร์ฟเวอร์หรือเครือข่ายขายปลีก และธุรกรรมจะถูกเก็บในฐานข้อมูลท้องถิ่นแบบออฟไลน์)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>When MPOS runs in Offline mode, it can't get images from the external image server to display from Retail Server, because Retail Server connectivity has been lost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อ MPOS รันในโหมดออฟไลน์ จะไม่สามารถเรียกรูปภาพจากเซิร์ฟเวอร์รูปภาพภายนอกเพื่อแสดงจากเซิร์ฟเวอร์ขายปลีกได้ เนื่องจากการเชื่อมต่อกับเซิร์ฟเวอร์ขายปลีกสูญหาย</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>However, you can still set up images so that they are shown when MPOS runs in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม คุณยังคงสามารถตั้งค่ารูปภาพเพื่อที่จะถูกแสดงเมื่อ MPOS รันในโหมดออฟไลน์ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Set up product images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้งค่ารูปภาพผลิตภัณฑ์เพื่อที่จะปรากฏขึ้นในโหมดออฟไลน์สำหรับ MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The product images that must be used in Offline mode can be set up by uploading the required physical image into the base product image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รูปภาพผลิตภัณฑ์ที่ต้องถูกใช้ในโหมดออฟไลน์สามารถตั้งค่าได้โดยการอัพโหลดรูปภาพทางกายภาพที่จำเป็นไปยังรูปภาพผลิตภัณฑ์พื้นฐาน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Click <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Products<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Products<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>การจัดการข้อมูลผลิตภัณฑ์<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ผลิตภัณฑ์<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ผลิตภัณฑ์<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select the product to set the offline image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เลือกผลิตภัณฑ์เพื่อตั้งค่ารูปภาพสำหรับข้อมูลออฟไลน์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and then click the arrow in the right corner to show the right pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คลิก <bpt id="p1">**</bpt>แก้ไข<ept id="p1">**</ept> และจากนั้นคลิกลูกศรในมุมด้านขวาเพื่อแสดงบานหน้าต่างด้านขวา</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>On the <bpt id="p1">**</bpt>Product image<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Change image<ept id="p2">**</ept>, and upload the physical image to use for the selected product in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในแท็บด่วน <bpt id="p1">**</bpt>รูปภาพผลิตภัณฑ์<ept id="p1">**</ept> คลิก <bpt id="p2">**</bpt>เปลี่ยนรูป<ept id="p2">**</ept> และอัพโหลดรูปภาพทางกายภาพเพื่อที่จะใช้สำหรับผลิตภัณฑ์ที่ถูกเลือกอยู่ในโหมดออฟไลน์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Save and close the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บันทึกและปิดหน้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>While MPOS is in Online mode, run the Catalog job in HQ, to make sure that the data is sent at least one time to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ขณะที่ MPOS อยู่ในโหมดออนไลน์ รันงานแค็ตตาล็อกแบบ HQ เพื่อให้แน่ใจว่าข้อมูลจะถูกส่งอย่างน้อยหนึ่งครั้งไปยังฐานข้อมูลแบบออฟไลน์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Put MPOS into Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตั้ง MPOS เป็นโหมดออฟไลน์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>You should see the image that you uploaded for the specific product in HQ.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">คุณควรเห็นรูปภาพที่คุณได้อัพโหลดสำหรับผลิตภัณฑ์เฉพาะแบบ HQ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Product image in Offline mode<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>รูปภาพของผลิตภัณฑ์ในโหมดออฟไลน์<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Set up catalog, category, employee, and customer images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ตั้งค่าแค็ตตาล็อก ประเภท และ พนักงานลูกค้ารูปเพื่อที่จะปรากฏขึ้นในโหมดออฟไลน์สำหรับ MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The catalog, category, employee, and customer images that must be used in Offline mode can be set up by adding the required image's destination link to the gallery and setting the image as the default image for the selected entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แค็ตตาล็อก ประเภท พนักงาน และรูปภาพของลูกค้าที่ต้องถูกใช้ในโหมดออฟไลน์สามารถตั้งค่าโดยการเพิ่มลิงค์ปลายทางของรูปภาพจำเป็นไปยังแกลเลอรี และตั้งค่ารูปภาพเป็นรูปภาพเริ่มต้นสำหรับเอนทิตี้ที่ถูกเลือก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Go to the catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปยังแค็ตตาล็อก และจากนั้น บนบานหน้าต่างการดำเนินการ คลิก <bpt id="p1">**</bpt>สื่อ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>รูปภาพ<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Follow the steps in the <bpt id="p1">[</bpt>Overwrite from the entity-level Preview page<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> section to add the external image URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทำตามขั้นตอนในส่วน <bpt id="p1">[</bpt>บันทึกทับจากหน้าการแสดงตัวอย่างระดับเอนทิตี<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> เพื่อที่จะเพิ่ม URL ของรูปภาพภายนอก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Mark this image as the default image for the catalog by selecting the check box against the Image listed in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ทำเครื่องหมายรูปภาพนี้เป็นรูปภาพเริ่มต้นสำหรับแค็ตตาล็อกโดยการเลือกกล่องกาเครื่องหมายสำหรับรูปภาพที่ถูกแสดงรายการอยู่ในกริด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Run the Catalog job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">รันงานแค็ตตาล็อก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>This image will now be used as the Offline image for that catalog in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ขณะนี้รูปภาพนี้จะถูกใช้เป็นรูปภาพแบบออฟไลน์สำหรับแค็ตตาล็อกนั้นใน MPOS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Follow a similar process for other entities, such as Category, Employee, and Customer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ทำตามกระบวนการที่คล้ายกันสำหรับเอนทิตีอื่น เช่น ประเภท พนักงาน และลูกค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline image<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>รูปภาพแบบออฟไลน์<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>