<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="Notifications-POS.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>Notifications-POS.74d2b9.6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6c813cfea9b570e8dfd5dbe7f3ca1f4ba8594420</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\Notifications-POS.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แสดงการแจ้งเตือนใบสั่งในการขายหน้าร้าน (POS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to enable order notifications in the point of sale and the notification framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หัวข้อนี้อธิบายวิธีการเปิดใช้งานการแจ้งเตือนใบสั่งในจุดขายหน้าร้าน และกรอบงานการแจ้งเตือน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Show order notifications in the point of sale (POS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แสดงการแจ้งเตือนใบสั่งในการขายหน้าร้าน (POS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In the modern retail environment, store associates are assigned various tasks, such as helping customers, entering transactions, doing stock counts, and receiving orders in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในสภาพแวดล้อมการขายปลีกสมัยใหม่ สมาคมร้านค้าได้รับมอบหมายงานต่างๆ เช่น การช่วยเหลือลูกค้า การป้อนธุรกรรม การดำเนินการตรวจนับสินค้าคงคลัง และการรับใบสั่งในร้านค้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The point of sale (POS) client provides a single application where associates can perform all these tasks and many others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไคลเอนต์จุดขายหน้าร้าน (POS) มีแอพลิเคชันเดียวที่ซึ่งสมาคมสามารถทำงานเหล่านี้และอื่นๆ อีกมากมายได้ทั้งหมด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Because various tasks must be performed during the day, associates might have to be notified when something requires their attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เนื่องจากงานต่างๆ ต้องถูกดำเนินการในระหว่างวัน สมาคมอาจต้องได้รับการแจ้งเตือน เมื่อบางอย่างต้องการการพิจารณาของพวกเขา</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The notification framework in the POS helps by letting retailers configure role-based notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กรอบงานการแจ้งเตือนใน POS ช่วยโดยการอนุญาตให้ผู้ค้าปลีกสามารถตั้งค่าคอนฟิกการแจ้งเตือนตามบทบาทได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In Microsoft Dynamics 365 for Retail with application update 5, these notifications can be configured only for POS operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ใน Microsoft Dynamics 365 for Retail ที่มีการปรับปรุงแอพลิเคชัน 5 การแจ้งเตือนเหล่านี้สามารถถูกตั้งค่าคอนฟิกได้เฉพาะสำหรับการดำเนินการ POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Currently, the system can show notifications only for order fulfillment operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในปัจจุบัน ระบบสามารถแสดงการแจ้งเตือนสำหรับการดำเนินการเติมสินค้าตามใบสั่งเท่านั้นได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, because the framework is designed to be extensible, developers will eventually be able to write a notification handler for any operation and show the notifications for that operation in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม เนื่องจากกรอบงานมีวัตถุประสงค์เพื่อให้สามารถขยายได้ ในขั้นสุดท้าย นักพัฒนาจะสามารถเขียนตัวจัดการการแจ้งเตือนสำหรับการดำเนินการใดๆ และแสดงการแจ้งเตือนสำหรับการดำเนินงานนั้นใน POS ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Enable notifications for order fulfillment operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เปิดใช้งานการแจ้งเตือนสำหรับการดำเนินการเติมสินค้าตามใบสั่ง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To enable notifications for order fulfillment operations, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการเปิดใช้งานการแจ้งเตือนสำหรับการดำเนินการเติมสินค้าตามใบสั่ง ให้ทำตามขั้นตอนเหล่านี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Operations<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปที่ <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>การตั้งค่าช่องทาง<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>การตั้งค่า POS<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>การดำเนินงาน<ept id="p5">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Search for the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> operation, and select the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for it to specify that the notification framework should listen to the handler for this operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ค้นหาการดำเนินงาน <bpt id="p1">**</bpt>การเติมสินค้าตามใบสั่ง<ept id="p1">**</ept> และเลือกกล่องกาเครื่องหมาย <bpt id="p2">**</bpt>เปิดใช้งานการแจ้งเตือน<ept id="p2">**</ept> เพื่อระบุว่ากรอบงานการแจ้งเตือนควรฟังตัวจัดการสำหรับการดำเนินงานนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If the handler is implemented, notifications for this operation will then be shown in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้ามีการใช้ตัวจัดการ การแจ้งเตือนสำหรับการดำเนินการนี้จะถูกแสดงใน POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Employees<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Workers<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph>, under Retail tab, open the POS permissions associated with the worker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปยัง <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>พนักงาน<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>ผู้ปฏิบัติงาน<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> ภายใต้แท็บการขายปลีก เปิดสิทธิ์ POS ที่เชื่อมโยงกับผู้ปฏิบัติงาน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Expand the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, add the <bpt id="p2">**</bpt>Order fulfillment<ept id="p2">**</ept> operation, and set the <bpt id="p3">**</bpt>Display order<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>1<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ขยาย FastTab <bpt id="p1">**</bpt>การแจ้งเตือน<ept id="p1">**</ept> เพิ่มการดำเนินงาน <bpt id="p2">**</bpt>การเติมสินค้าตามใบสั่ง<ept id="p2">**</ept> และตั้งค่าฟิลด์ <bpt id="p3">**</bpt>ลำดับการแสดงผล<ept id="p3">**</ept> เป็น <bpt id="p4">**</bpt>1<ept id="p4">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If more than one notification is configured, this field is used to arrange the notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถ้ามีการตั้งค่าคอนฟิกการแจ้งเตือนมากกว่าหนึ่งรายการ ฟิลด์นี้จะถูกใช้เพื่อจัดการการแจ้งเตือน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Notifications that have a lower <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value appear above notifications that have a higher value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การแจ้งเตือนที่มีที่ค่า <bpt id="p1">**</bpt>ลำดับการแสดงผล<ept id="p1">**</ept> ที่ต่ำกว่า ปรากฏขึ้นเหนือการแจ้งเตือนที่มีค่าสูงกว่า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Notifications that have a <bpt id="p1">**</bpt>Display order<ept id="p1">**</ept> value of <bpt id="p2">**</bpt>1<ept id="p2">**</ept> are at the top.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การแจ้งเตือนที่มีค่า <bpt id="p1">**</bpt>ลำดับการแสดงผล<ept id="p1">**</ept> เป็น <bpt id="p2">**</bpt>1<ept id="p2">**</ept> อยู่ที่ด้านบนสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Notifications are shown only for operations that are added on the <bpt id="p1">**</bpt>Notifications<ept id="p1">**</ept> FastTab, and you can add operations there only if the <bpt id="p2">**</bpt>Enable notifications<ept id="p2">**</ept> check box for those operations has been selected on the <bpt id="p3">**</bpt>POS operations<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การแจ้งเตือนจะถูกแสดงเฉพาะสำหรับการดำเนินงานที่ถูกเพิ่มลงใน FastTab <bpt id="p1">**</bpt>การแจ้งเตือน<ept id="p1">**</ept> และคุณสามารถเพิ่มการดำเนินงานได้ เฉพาะเมื่อมีการเลือกกล่องกาเครื่องหมาย <bpt id="p2">**</bpt>เปิดใช้งานการแจ้งเตือน<ept id="p2">**</ept> สำหรับการดำเนินการดังกล่าวในหน้า <bpt id="p3">**</bpt>การดำเนินงาน POS<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Additionally, notifications for an operation are shown to workers only if the operation is added to the POS permissions for those workers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">นอกจากนี้ การแจ้งเตือนสำหรับการดำเนินงานจะถูกแสดงแก่ผู้ปฏิบัติงาน เฉพาะเมื่อมีการเพิ่มการดำเนินงานไปยังสิทธิ์ของ POS สำหรับผู้ปฏิบัติงานเหล่านั้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Notifications can be overridden at the user level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การแจ้งเตือนสามารถถูกแทนที่ได้ที่ระดับผู้ใช้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open the worker's record, select <bpt id="p1">**</bpt>POS permissions<ept id="p1">**</ept>, and then edit the user's notification subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เปิดเรกคอร์ดผู้ปฏิบัติงาน เลือก <bpt id="p1">**</bpt>สิทธิ์ของ POS<ept id="p1">**</ept> และจากนั้นแก้ไขการบอกรับเป็นสมาชิกการแจ้งเตือนของผู้ใช้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>POS profiles<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>Functionality profiles<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปยัง <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>การตั้งค่าช่องสัทาง<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>การตั้งค่า POS<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>โปรไฟล์ POS<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>โพรไฟล์ฟังก์ชัน<ept id="p5">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the <bpt id="p1">**</bpt>Notification interval<ept id="p1">**</ept> field, specify how often notifications should be pulled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในฟิลด์ <bpt id="p1">**</bpt>ช่วงการแจ้งเตือน<ept id="p1">**</ept> ระบุความถี่ที่ควรดึงการแจ้งเตือน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For some notifications, the POS must make real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับการแจ้งเตือนบางรายการ POS ต้องทำการเรียกใช้แบบเรียลไทม์ไปยังแอพลิเคชันฝ่ายสนับสนุน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>These calls consume the compute capacity of your back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การเรียกใช้เหล่านี้ใช้กำลังการผลิตที่คำนวณของแอพลิเคชันฝ่ายสนับสนุนของคุณ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Therefore, when you set the notification interval, you should consider both your business requirements and the impact of real-time calls to the back-office application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดังนั้น เมื่อคุณตั้งค่าช่วงเวลาของการแจ้งเตือน คุณควรพิจารณาทั้งความต้องการทางธุรกิจของคุณและผลกระทบของการเรียกใช้แบบเรียลไทม์ไปยังแอพลิเคชันฝ่ายสนับสนุน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>A value of <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (zero) turns off notifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ค่าเป็น <bpt id="p1">**</bpt>0<ept id="p1">**</ept> (ศูนย์) จะปิดการแจ้งเตือน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไปที่ <bpt id="p1">**</bpt>การขายปลีก<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ไอทีการขายปลีก<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>กำหนดการกระจาย<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Select the <bpt id="p1">**</bpt>1060<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Staff<ept id="p2">**</ept>) schedule to synchronize notification subscription settings, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เลือกกำหนดการ <bpt id="p1">**</bpt>1060<ept id="p1">**</ept> (<bpt id="p2">**</bpt>พนักงาน<ept id="p2">**</ept>) เพื่อซิงค์การตั้งค่าการบอกรับเป็นสมาชิกการแจ้งเตือน แล้วจากนั้นเลือก <bpt id="p3">**</bpt>รันทันที<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Next, select the <bpt id="p1">**</bpt>1070<ept id="p1">**</ept> (<bpt id="p2">**</bpt>Channel configuration<ept id="p2">**</ept>) schedule to synchronize the permission interval, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากนั้น เลือกกำหนดการ <bpt id="p1">**</bpt>1070<ept id="p1">**</ept> (<bpt id="p2">**</bpt>การตั้งค่าคอนฟิกช่องทาง<ept id="p2">**</ept>) เพื่อซิงค์ช่วงของสิทธิ์ แล้วจากนั้นคลิก <bpt id="p3">**</bpt>รันทันที<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>View notifications in the POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดูการแจ้งเตือนใน POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>After you complete the preceding steps, the workers will be able to view the notifications in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">หลังจากที่คุณทำขั้นตอนก่อนหน้าเสร็จแล้ว ผู้ปฏิบัติงานจะสามารถดูการแจ้งเตือนใน POS ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>To view notifications, press the notification icon in the top right corner of the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อดูการแจ้งเตือน กดไอคอนการแจ้งเตือนในมุมขวาบนของ POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>A notification center appears and shows notifications for the order fulfillment operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ศูนย์การแจ้งเตือนจะปรากฎ และแสดงการแจ้งเตือนสำหรับการดำเนินการเติมสินค้าตามใบสั่ง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The notification center should show the following groups in the order fulfillment operation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ศูนย์การแจ้งเตือนควรแสดงกลุ่มต่อไปนี้ในการดำเนินการเติมสินค้าตามใบสั่ง:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Store pickup<ept id="p1">**</ept> – This group shows the count of orders that have a delivery mode of <bpt id="p2">**</bpt>Pickup<ept id="p2">**</ept>, and that are scheduled for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>การเบิกสินค้าของร้านค้า<ept id="p1">**</ept> – กลุ่มนี้แสดงการตรวจนับของใบสั่งที่มีโหมดการจัดส่งเป็น <bpt id="p2">**</bpt>เบิกสินค้า<ept id="p2">**</ept> และที่มีการจัดกำหนดการการเบิกสินค้าจากร้านค้าปัจจุบัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถกดหมายเลขบนกลุ่มเพื่อเปิดหน้า <bpt id="p1">**</bpt>การเติมสินค้าตามใบสั่ง<ept id="p1">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for pickup from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกรณีนี้ คุณจะสามารถกรองหน้าเพื่อให้แสดงเฉพาะใบสั่งที่ใช้งานอยู่ ซึ่งถูกตั้งค่าสำหรับการเบิกสินค้าจากร้านค้าปัจจุบัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Ship from store<ept id="p1">**</ept> – This group shows the count of orders that have the delivery mode of <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept>, and that are scheduled for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ส่งจากร้านค้า<ept id="p1">**</ept> – กลุ่มนี้แสดงการตรวจนับของใบสั่งที่มีโหมดการจัดส่งเป็น <bpt id="p2">**</bpt>การจัดส่ง<ept id="p2">**</ept> และที่มีการจัดกำหนดการสำหรับการจัดส่งจากร้านค้าปัจจุบัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>You can press the number on the group to open the <bpt id="p1">**</bpt>Order fulfillment<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถกดหมายเลขบนกลุ่มเพื่อเปิดหน้า <bpt id="p1">**</bpt>การเติมสินค้าตามใบสั่ง<ept id="p1">**</ept> ได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>In this case, the page will be filtered so that it shows only the active orders that are set up for shipment from the current store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกรณีนี้ คุณจะสามารถกรองหน้าเพื่อให้แสดงเฉพาะใบสั่งที่ใช้งานอยู่ ซึ่งถูกตั้งค่าสำหรับการจัดส่งจากร้านค้าปัจจุบัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>When new orders are assigned to the store for fulfillment, the notification icon changes to indicate that there are new notifications, and the count for the appropriate groups is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อมีการกำหนดใบสั่งใหม่ให้กับร้านค้าสำหรับการเติมสินค้า ไอคอนการแจ้งเตือนจะเปลี่ยนเพื่อบ่งชี้ว่า มีการแจ้งเตือนใหม่และจำนวนสำหรับกลุ่มที่เหมาะสมจะถูกปรับปรุง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Even though the groups are refreshed at regular intervals however, POS users can manually refresh the groups at any time by selecting the <bpt id="p1">**</bpt>Refresh<ept id="p1">**</ept> button next to the group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แม้ว่าจะมีการรีเฟรชกลุ่มที่ช่วงสม่ำเสมอ อย่างไรก็ตาม ผู้ใช้ POS สามารถรีเฟรชกลุ่มด้วยตนเองได้ตลอดเวลา โดยการเลือกปุ่ม <bpt id="p1">**</bpt>รีเฟรช<ept id="p1">**</ept> ถัดจากกลุ่ม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Lastly, if a group has a new item, that the current worker hasn't viewed, then the group shows a burst symbol to indicate new content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สุดท้าย ถ้ากลุ่มมีสินค้าใหม่ที่ผู้ปฏิบัติงานปัจจุบันยังไม่ได้ดู จากนั้นกลุ่มแสดงสัญลักษณ์ระเบิดเพื่อบ่งชี้เนื้อหาใหม่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Enable live content on POS buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เปิดใช้งานเนื้อหาขณะใช้งานจริงบนปุ่ม POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>POS buttons can now show a count to help workers easily determine which tasks require their immediate attention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ขณะนี้ปุ่ม POS สามารถแสดงการนับได้ เพื่อช่วยให้ผู้ปฏิบัติงานสามารถกำหนดได้อย่างง่ายดาย ว่างานใดต้องการความสนใจของพวกเขาในทันที</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>To show this number on a POS button, you must complete the notification setup that is described earlier in this topic (that is, you must enable notifications for an operation, set up a notification interval, and update the POS permission group for the worker).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในการแสดงหมายเลขนี้บนปุ่ม POS คุณต้องดำเนินการตั้งค่าการแจ้งเตือนที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้ให้เสร็จสมบูรณ์ (นั่นคือ คุณต้องเปิดใช้งานการแจ้งเตือนสำหรับการดำเนินงาน ตั้งค่าช่วงการแจ้งเตือน และอัพเดกลุ่มสิทธิ์ของ POS สำหรับผู้ปฏิบัติงาน)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Additionally, you must open the button grid designer, view the button's properties, and select the <bpt id="p1">**</bpt>Enable live content<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">นอกจากนี้ คุณต้องเปิดโปรแกรมออกแบบกริดปุ่ม ดูคุณสมบัติของปุ่ม และเลือกกล่องกาเครื่องหมาย <bpt id="p1">**</bpt>เปิดใช้งานเนื้อหาขณะใช้งานจริง<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In the <bpt id="p1">**</bpt>Content alignment<ept id="p1">**</ept> field, you can select whether the count appears in the upper-right corner of the button (<bpt id="p2">**</bpt>Top right<ept id="p2">**</ept>) or in the center (<bpt id="p3">**</bpt>Center<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในฟิลด์ <bpt id="p1">**</bpt>การจัดแนวเนื้อหา<ept id="p1">**</ept> คุณสามารถเลือกได้ว่าการตรวจนับจะปรากฏในมุมบนด้านขวาของปุ่มหรือไม่ (<bpt id="p2">**</bpt>ด้านบนขวา<ept id="p2">**</ept>) หรือกึ่งกลาง (<bpt id="p3">**</bpt>กึ่งกลาง<ept id="p3">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The live content can be enabled for operations only if the <bpt id="p1">**</bpt>Enable notifications<ept id="p1">**</ept> check box has been selected for them on the <bpt id="p2">**</bpt>POS operations<ept id="p2">**</ept> page, as described earlier in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เนื้อหาขณะใช้งานจริงอาจต้องถูกเปิดใช้งานสำหรับการดำเนินงาน ก็ต่อเมื่อมีการเลือกกล่องกาเครื่องหมาย <bpt id="p1">**</bpt>เปิดใช้งานการแจ้งเตือน<ept id="p1">**</ept> ไว้ในหน้า <bpt id="p2">**</bpt>การดำเนินงาน POS<ept id="p2">**</ept> ตามที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The following illustration shows the live content settings in the button grid designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ภาพประกอบต่อไปนี้แสดงการตั้งค่าเนื้อหาขณะใช้งานจริงในโปรแกรมออกแบบกริดปุ่ม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">![</bpt>Live content settings in the button grid designer<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>Live content settings in the button grid designer<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>การตั้งค่าเนื้อหาขณะใช้งานจริงในโปรแกรมออกแบบกริดปุ่ม<ept id="p1">]</ept><bpt id="p2">(./media/ButtonGridDesigner.png "</bpt>การตั้งค่าเนื้อหาขณะใช้งานจริงในโปรแกรมออกแบบกริดปุ่ม<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To show the notification count on a button, you need to ensure that the correct screen layout is being updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการแสดงจำนวนการแจ้งเตือนบนปุ่ม คุณต้องตรวจสอบให้แน่ใจว่ามีการอัพเดตโครงร่างหน้าจอที่ถูกต้อง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>To determine the screen layout that is being used by the POS, select the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> icon in upper-right corner and note the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการกำหนดโครงร่างหน้าจอที่มีการใช้งานโดย POS เลือกไอคอน <bpt id="p1">**</bpt>การตั้งค่า<ept id="p1">**</ept> ในมุมด้านขวาบน และบันทึก <bpt id="p2">**</bpt>รหัสโครงร่างหน้าจอ<ept id="p2">**</ept> และ <bpt id="p3">**</bpt>ความละเอียดของโครงร่าง<ept id="p3">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Now using Edge browser, go to the <bpt id="p1">**</bpt>Screen layout<ept id="p1">**</ept> page in Dynamics 365 for Finance and Operations, find the <bpt id="p2">**</bpt>Screen layout ID<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Layout resolution<ept id="p3">**</ept> identified above and select the <bpt id="p4">**</bpt>Enable live content<ept id="p4">**</ept> check box.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ขณะนี้โดยใช้เบราว์เซอร์ Edge ให้ไปที่หน้า <bpt id="p1">**</bpt>โครงร่างหน้าจอ<ept id="p1">**</ept> ใน Dynamics 365 for Finance and Operations ค้นหา <bpt id="p2">**</bpt>รหัสโครงร่างหน้าจอ<ept id="p2">**</ept> และ <bpt id="p3">**</bpt>ความละเอียดโครงร่าง<ept id="p3">**</ept> ที่ระบุด้านบน และเลือกกล่องกาเครื่องหมาย <bpt id="p4">**</bpt>เปิดใช้งานเนื้อหาที่ใช้งานจริง<ept id="p4">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> Distribution schedule<ept id="p1">**</ept> and run the 1090 (Registers) job to synchronize layout changes.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">ไปที่ <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> กำหนดการกระจาย<ept id="p1">**</ept> และรันงาน 1090 (เครื่องบันทึกเงินสด) เพื่อซิงโครไนส์การเปลี่ยนแปลงโครงร่าง</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">![</bpt>Find the screen layout used by POS<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>Find the screen layout <ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>ค้นหาโครงร่างหน้าจอที่ใช้โดย POS<ept id="p1">]</ept><bpt id="p2">(./media/Choose_screen_layout.png "</bpt>ค้นหาโครงร่างหน้าจอ <ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The following illustration shows the effect of selecting <bpt id="p1">**</bpt>Top right<ept id="p1">**</ept> versus <bpt id="p2">**</bpt>Center<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>Content alignment<ept id="p3">**</ept> field for buttons of various sizes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ภาพประกอบต่อไปนี้แสดงผลของการเลือก <bpt id="p1">**</bpt>ด้านบนขวา<ept id="p1">**</ept> เทียบกับ <bpt id="p2">**</bpt>กึ่งกลาง<ept id="p2">**</ept> ในฟิลด์ <bpt id="p3">**</bpt>การจัดแนวเนื้อหา<ept id="p3">**</ept> สำหรับปุ่มขนาดต่างๆ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">![</bpt>Live content on POS buttons<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>Live content on POS buttons<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>เนื้อหาขณะใช้งานจริงบนปุ่ม POS<ept id="p1">]</ept><bpt id="p2">(./media/ButtonsWithLiveContent.png "</bpt>เนื้อหาขณะใช้งานจริงบนปุ่ม POS<ept id="p2">")</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>