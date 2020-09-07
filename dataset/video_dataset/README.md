# The SoccerDB video dataset
## [SoccerDB2SoccerNet.csv](https://github.com/newsdata/SoccerDB/blob/master/dataset/video_dataset/SoccerDB2SoccerNet.csv)
### The comparison table of SoccerDB to SoccerNet. The first column is the video name of SoccerDB. The second column is the video name of SoccerNet, and if it is null, it is the video that belongs to SoccerDB alone. It is stored in the Baidu network disk.
### https://pan.baidu.com/s/1YaIhrKy7OuuWDviih5SCXA code: h4ca
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
### lmdb: https://pan.baidu.com/s/1KLdoLsJGtnKnWQE9QMX1ow code: d67n
### offset: offset of frames in video. type: np.int16 shape: 1~64
### length: number of Effective bbox for frame. type: np.int8 shape: 1~64
### bboxes: info of bboxes. type: np.int16 shape (offset_shape, 32, 4)
### ids: class of bbox.
### score: confidence of bbox.

 keys | state | type | shape | comment | Complete the keys |
 ---- | ---- | ---- | ---- | ---- | ---- |
 offset | offset of frames in video | np.int16 |
 ---- | ---- | ---- | ---- | ---- | ---- |
 length | number of Effective bbox for each frame| np.int8 |
 ---- | ---- | ---- | ---- | ---- | ---- |
 bboxes | info of bboxes | np.int16 |
 ---- | ---- | ---- | ---- | ---- | ---- |
 ids | class of bboxes | np.int8 |
 ---- | ---- | ---- | ---- | ---- | ---- |
 score | score of bboxes | np.float32 |

