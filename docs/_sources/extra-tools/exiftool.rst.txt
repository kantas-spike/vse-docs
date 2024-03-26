ExifTool
********

.. All image, video and audio files contain metadata, e.g. the CreationDate of the image, the Camera type, GPS coordinates, ... With ExifTool, you can read and sometimes also update (write) these metadata.

すべての画像、ビデオ、オーディオ ファイルには、画像の作成日、カメラの種類、GPS 座標などのメタデータが含まれています。ExifTool を使用すると、これらのメタデータを読み取り、場合によっては更新 (書き込み) することもできます。

.. Change the creation date of a video
動画の作成日を変更する
===================================

.. Sometimes the date and time are not set correctly in a camera (for example, when switching time zones). When shooting a video with this camera, the metadata will not represent the actual date the video was shot.  For example, the video test.mov (see below) was shot on 2021-08-05 with a smartphone, but due to a previous factory reset the date was incorrectly set as 2019-11-01 within the phone.

カメラの日付と時刻が正しく設定されない場合があります（タイムゾーンを切り替える場合など）。このカメラでビデオを撮影する場合、メタデータはビデオが撮影された実際の日付を表しません。たとえば、ビデオ "test.mov" (下記を参照) はスマートフォンで 2021 年 8 月 5 日に撮影されましたが、以前の工場出荷時設定へのリセットにより、スマートフォン内で日付が誤って 2019 年 11 月 1 日に設定されました。

.. This particular smartphone recorded several date and time fields within the test.mov file. The following command will display all the date & time info that is available within test.mov.

この特定のスマートフォンは、"test.mov" ファイル内にいくつかの日付と時刻のフィールドを記録しました。次のコマンドは、"test.mov" 内で利用可能なすべての日付と時刻の情報を表示します。


``exiftool -time:all -groupNames -short test.mov``

..
  - *time:all*: shortcut to display all metadata fields that contain date/time info
  - *groupNames*: print the group name in front of each tag
  - *short*: tag names are printed instead of descriptions.
..
- *time:all*: 日付/時刻情報を含むすべてのメタデータ フィールドを表示するショートカット
- *groupNames*: 各タグの前にグループ名を出力します。
- *short*: 説明の代わりにタグ名が表示されます。

.. code-block:: none

   [File]          FileModifyDate                  : 2019:11:01 22:22:22+01:00
   [File]          FileAccessDate                  : 2021:08:07 16:29:11+02:00
   [File]          FileCreateDate                  : 2021:08:07 16:29:05+02:00
   [QuickTime]     CreateDate                      : 2019:11:01 21:22:22
   [QuickTime]     ModifyDate                      : 2019:11:01 21:22:30
   [QuickTime]     TrackCreateDate                 : 2019:11:01 21:22:22
   [QuickTime]     TrackModifyDate                 : 2019:11:01 21:22:30
   [QuickTime]     MediaCreateDate                 : 2019:11:01 21:22:22
   [QuickTime]     MediaModifyDate                 : 2019:11:01 21:22:30
   [QuickTime]     CreationDate                    : 2019:11:01 22:22:22+01:00

.. There are two group names [File] and [QuickTime]. The first group of tags is usually managed by the operating system of the device. For example, you can see that the file test.mov is apparently copied from the smartphone to a desktop on 2021-08-07; while the other dates (due to the wrong date/time settings in the smartphone) are set to 2019-11-01. The [QuickTime] tags are set by the smartphone (in this case an Apple iPhone).

グループ名は[File]と[QuickTime]の2つがあります。タグの最初のグループは通常、デバイスのオペレーティング システムによって管理されます。
たとえば、ファイル "test.mov" は 2021 年 8 月 7 日にスマートフォンからデスクトップにコピーされたようです。一方、他の日付（スマートフォンの日付/時刻設定が間違っているため）は 2019-11-01 に設定されます。[QuickTime]タグはスマートフォン（この場合はApple iPhone）によって設定されます。

.. To update a time-field, for example the [QuickTime] CreateDate, you can use the Shift command.
[QuickTime] CreateDate などの時間フィールドを更新するには、Shift コマンドを使用できます。

``exiftool "-QuickTime:CreateDate += 0000:21:04 00:00:00"  testing.mov``

.. The metadata field *QuickTime:CreateDate* is incremented with 0 years, 21 months and 4 days, resetting 2019-11-01 to 2021-08-05. The command will make a copy of the original file with the name testing.mov_original and update the field in testing.mov.

メタデータ フィールドQuickTime:CreateDate は0 年、21 か月、4 日ずつ増分され、2019 年 11 月 1 日から 2021 年 8 月 5 日にリセットされます。このコマンドは、testing.mov_original という名前で元のファイルのコピーを作成し、 "testing.mov" 内のフィールドを更新します。

.. To update all the [QuickTime] time-fields, you can use the following command:
すべての [QuickTime] 時間フィールドを更新するには、次のコマンドを使用できます。

``exiftool "-QuickTime:time:all += 0000:21:04 00:00:00"  testing.mov``

.. This will result in the following update of the file testing.mov. Because the previous command runned at 2021:08:08 16:01:44+02:00, the [File] tags are updated consequently by the operating system.

これにより、"testing.mov" ファイルが次のように更新されます。前のコマンドは 2021:08:08 16:01:44+02:00 に実行されたため、[File] タグはオペレーティング システムによって更新されます。

.. code-block:: none

   [File]          FileModifyDate                  : 2021:08:08 16:01:44+02:00
   [File]          FileAccessDate                  : 2021:08:08 16:01:44+02:00
   [File]          FileCreateDate                  : 2021:08:07 16:29:05+02:00
   [QuickTime]     CreateDate                      : 2021:08:05 21:22:22
   [QuickTime]     ModifyDate                      : 2021:08:05 21:22:30
   [QuickTime]     TrackCreateDate                 : 2021:08:05 21:22:22
   [QuickTime]     TrackModifyDate                 : 2021:08:05 21:22:30
   [QuickTime]     MediaCreateDate                 : 2021:08:05 21:22:22
   [QuickTime]     MediaModifyDate                 : 2021:08:05 21:22:30
   [QuickTime]     CreationDate                    : 2021:08:05 22:22:22+01:00

.. To set the all [QuickTime] date & time metadata to as specific time, you can use the following command. As explained above, the [File] tags will not be updated to this specific time.

すべての [QuickTime] 日付と時刻メタデータを特定の時刻として設定するには、次のコマンドを使用できます。上で説明したように、[File] タグはこの特定の時刻に更新されません。

``exiftool -wm w -QuickTime:time:all="2022:08:05 23:12:12" testing.mov``
