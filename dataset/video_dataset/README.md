# The SoccerDB video dataset
## [SoccerDB2SoccerNet.csv](https://github.com/newsdata/SoccerDB/blob/master/dataset/video_dataset/SoccerDB2SoccerNet.csv)
### The comparison table of SoccerDB to SoccerNet. The first column is the video name of SoccerDB. The second column is the video name of SoccerNet, and if it is null, it is the video that belongs to SoccerDB alone. 
### SoccerDB Videos:
### 1. Videos of SoccerNet: Application from [SoccerNet](https://soccer-net.org/)
### 2. Videos of SoccerDB: fill the [form](https://github.com/newsdata/SoccerDB/raw/master/dataset/SoccerDB_agreement_form.doc) and send PDF format to cuikaixu@shuwen.com(links provided after agreeing with the [Xinhua Zhiyun Technology Co. LTD](https://www.xinhuazhiyun.com/) )
## [seg_info.csv](https://github.com/newsdata/SoccerDB/blob/master/dataset/video_dataset/seg_info.csv)
### The information table of the video segment.
### seg_id: Key for video segments.
### video_name: The video source of the video segment.
### start_time: The start time of the video segment.
### end_time: The end time of the video segment.
### event_start_time: The start time of the event.
### event_end_time: The end time of the event.
### cls_id: Category of events.

 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
 ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
 Background | Injured | Red/Yellow Card | Shot | Substitution | Free Kick | Corner | Saves | Penalty Kick | Foul | Goal |
### highlight_cls: Category of highlight.
 0 | 1 | 2 | 3 |
 ---- | ---- | ---- | ---- |
 Not highlight | Playback | Segments that are played back | Goal |

## [train_seg_key.csv](https://github.com/newsdata/SoccerDB/blob/master/dataset/video_dataset/train_seg_key.csv)
### Keys for train video segments.
## [val_seg_key.csv](https://github.com/newsdata/SoccerDB/blob/master/dataset/video_dataset/val_seg_key.csv)
### Keys for val video segments.
## Bounding box lmdb
### lmdb: https://pan.baidu.com/s/16XLPY4f-cctG5b6d5-j8pg code: n2ga

 keys | state | type | shape | complete the keys | comment |
 ---- | ---- | ---- | ---- | ---- | ---- |
 offset | offset of frames in video | np.int16 | 1~64 | ("%s_offset" % seg_key).encode() | _ |
 length | number of effective bbox for each frame| np.int8 | 1~64 | ("%s_length" % seg_key).encode() | _ |
 bboxes | info of bboxes x1, y1, x2, y2 | np.int16 | offset_shape, 32, 4 | ("%s_bboxes" % seg_key).encode() | each frame fixed 32 but effective is value of length|
 ids | class of bboxes | np.int8 | offset_shape, 32 | ("%s_ids" % seg_key).encode() | each frame fixed 32 but effective is value of length |
 score | score of bboxes | np.float32 | offset_shape, 32 | ("%s_score" % seg_key).encode() | each frame fixed 32 but effective is value of length |

