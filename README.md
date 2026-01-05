# ClipForge

A powerful desktop application for marking and extracting video clips with metadata annotation. Perfect for sports analysis, video annotation projects, research, and content creation.

![Python Version](https://img.shields.io/badge/python-3.7%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Maintained](https://img.shields.io/badge/maintained-yes-brightgreen)

## Features

### 🎬 Video Playback
- Support for multiple video formats (MP4, AVI, MKV, MOV)
- Smooth video playback with timeline scrubbing
- Variable playback speeds: -16x, -8x, -4x, -3x, -2x, -1x, 1x, 2x, 3x, 4x, 8x, 16x
- Forward and backward playback
- Precise frame-by-frame navigation

### ✂️ Clip Marking
- Mark start and end points for video clips
- Real-time timestamp display (HH:MM:SS.mmm)
- Visual feedback for marked segments
- Easy clip clearing and remarking

### 📝 Metadata Annotation
- **Action Class ID**: Categorize your clips
- **Description**: Add detailed descriptions
- **Team**: Track team-related information
- **Equipment**: Document equipment used
- All metadata exported to CSV

### 💾 Data Management
- Auto-save all marked clips as separate video files
- Export metadata to CSV for easy analysis
- **Load History**: Resume previous sessions
- Action logging with timestamps
- Smart clip numbering (continues from existing clips)
- Prevents duplicate clip saves

### 📊 Organization
- Clip list with sortable columns
- Action history viewer
- Delete unwanted clips before export
- Visual clip overview with all metadata

## Installation

### Prerequisites
- Python 3.7 or higher
- pip (Python package manager)

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/kunalsinha/clipforge.git
cd clipforge
```

2. **Install required packages**
```bash
pip install -r requirements.txt
```

3. **Run the application**
```bash
python clipforge.py
```

## Usage

### Getting Started

1. **Load a Video**
   - Click "Browse" next to Video Path
   - Select your video file
   - Click "Load" to open the video

2. **Set Save Directory**
   - Click "Browse" next to Save Path
   - Choose where to save your clips
   - If history exists, you'll be prompted to load it

3. **Mark Clips**
   - Navigate to the start of your desired clip
   - Click "⏺ Mark Start"
   - Navigate to the end of the clip
   - Click "⏹ Mark End"
   - Fill in metadata fields
   - Clip is automatically added to the list

4. **Save Everything**
   - Review your marked clips in the list
   - Click "💾 Save All Clips & Export CSV"
   - All clips and metadata will be saved to your directory

### Keyboard Shortcuts & Tips

- Use speed controls for quick navigation
- Negative speeds play backward
- Higher speeds (8x, 16x) are great for scanning long videos
- The timeline slider allows quick seeking
- Mark Start/End can be used multiple times to mark several clips

### Loading Previous Work

If you've previously worked on clips in a directory:
1. Browse to that directory
2. Click "Load History" (or accept the auto-prompt)
3. All previous clips and logs will be restored
4. New clips will continue numbering from where you left off

### Output Files

The application creates three types of files in your save directory:

1. **Video Clips**: `clip_1.mp4`, `clip_2.mp4`, etc.
2. **Metadata CSV**: `clips_metadata.csv` with columns:
   - S.No
   - Clip Name
   - Action Class ID
   - Start Time Stamp
   - End Time Stamp
   - Description
   - Team
   - Equipment

3. **Action Log**: `actions_log.txt` with timestamped history

## CSV Output Format

```csv
S.No,Clip Name,Action Class ID,Start Time Stamp,End Time Stamp,Description,Team,Equipment
1,clip_1.mp4,goal,00:05:23.450,00:05:28.120,Corner kick goal,Team A,Ball
2,clip_2.mp4,foul,00:12:45.230,00:12:50.890,Yellow card offense,Team B,None
```

## Troubleshooting

### Video Won't Load
- Ensure the video file exists and isn't corrupted
- Check that the video format is supported
- Try converting the video to MP4 format

### Playback Issues
- Lower the playback speed if frames are skipping
- Ensure your system has sufficient resources
- Check that OpenCV is properly installed

### Save Errors
- Verify you have write permissions in the save directory
- Ensure sufficient disk space
- Check that the video file is still accessible

## Technical Details

### Built With
- **tkinter**: GUI framework
- **OpenCV (cv2)**: Video processing
- **PIL (Pillow)**: Image handling
- **pandas**: Data management and CSV export

### Video Processing
- Uses OpenCV's VideoCapture for reading
- VideoWriter for clip extraction
- Maintains original video resolution and FPS

### Performance
- Threaded playback for smooth UI
- Efficient frame seeking
- Minimal memory footprint

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Keyboard shortcuts for mark start/end
- [ ] Clip preview before export
- [ ] Batch video processing
- [ ] Export to different video formats
- [ ] Video filters and effects
- [ ] Custom clip naming schemes
- [ ] Annotation overlays on video

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with Python and OpenCV
- Inspired by professional video annotation tools
- Thanks to all contributors

## Contact

**Author**: Kunal Sinha

For questions, issues, or suggestions:
- Open an issue on GitHub
- Email: shinakunal9153@gmail.com

---

**ClipForge** - Forging Perfect Clips, Frame by Frame 🎬
