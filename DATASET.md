# WYD data

There are three aspects to the WYD data:

- Dataset annotations
- Videos
- Video segmentation masks

## Dataset annotations

The dataset annotations are located within the [`wyd.json`](wyd.json) JSON file.
Each entry of the dataset contains the following information:

- `wyd_id` (str): unique identifier of the video
- `video_name` (str): name of the video in the corresponding dataset
- `dataset_name` (str): name of dataset the video originally belongs to
- `actor_name` (str): generic name of an actor (e.g., "man") from [VidLN](https://google.github.io/video-localized-narratives/)
- `vidln_id` (str): unique identifier of the video in [VidLN](https://google.github.io/video-localized-narratives/)
- `storybench_id` (str): unique identifier of the video in [StoryBench](https://github.com/google/storybench)
- `caption` (str): text description of the action happening in the video
- `start_frame` (int): index of the first frame from the original video that is used in our benchmark (relative to the first frame in the corresponding dataset)
- `end_frame` (int): index of the last frame from the original video that is used in our benchmark (relative to the first frame in the corresponding dataset)
- `video_length` (int): length of the video in frames
- `video_height` (int): height of the video in pixels
- `video_width` (int): width of the video in pixels
- `video_fps` (int): frame rate of the video
- `categories` (dict): a dictionary of human-labeled categories for the video
  - `actions` (list[str]): actions performed in the video (eg., sports)
  - `camera` (list[str]): camera motion in the video (ie., static/dynamic)
  - `flows` (list[str]): amount of motion in the video (higher values indicate more motion)
  - `interactions` (list[str]): types of interactions in the video (eg., objects)
  - `locomotions` (list[str]): types of locomotion in the video (eg., full-body)
  - `num_actors` (list[str]): Number of human actors in the video (ie., 1/2/3+)
  - `occlusions` (list[str]): Average level of occlusion of the human actors (higher values indicate more occlusion)
  - `scenes` (list[str]): Scene where the video takes place (eg., park)
  - `sizes` (list[str]): Average size of the human actors the video (higher values indicate larger frame coverage)

## Videos

We filter videos from existing publicly available datasets.
We redirect to the official sources to download them:

- [DiDeMo](https://github.com/LisaAnne/LocalizingMoments): see "Google Drive" link
- [Oops](https://oops.cs.columbia.edu/data/): see "Download" button
- [UVO](https://sites.google.com/corp/view/unidentified-video-object/): see "Dataset" tab

## Video segmentation masks

We will release the video segmentation masks of every human actor in each video.
