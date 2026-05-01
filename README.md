# IsoPhaseLab — XB7 RadioVision

**WiFi-based 3D RF Imaging & Sensing Platform**  
*Turning a consumer Xfinity XB7 modem (TG02DCW4482CT / Technicolor CGM4331COM) into a no-hardware radar for mapping solid objects, walls, furniture, and motion through multipath reflections.*

![Project Banner](https://via.placeholder.com/800x200/0A2540/00FFAA?text=IsoPhaseLab+%E2%80%94+RadioVision) <!-- Replace with real banner later -->

## 🎯 Vision

IsoPhaseLab is an open-source project that transforms an **WiFi 6 router** into a live RF sensing system. By analyzing signal strength fluctuations, multipath interference, and dielectric perturbations caused by physical objects, we create real-time visualizations and eventually 3D reconstructions — all without extra hardware.

Built by an engineer as a viral portfolio piece. **Zero oscilloscopes. Zero lab gear. Just Python, your laptop, and your XB7.**

## ✨ Core Features (Current & Planned)

### Phase 0.5 — Live Sensing Dashboard (Done)
- Real-time RSSI / signal strength polling via Windows `netsh`
- Beautiful Streamlit dashboard with live plots and disturbance detection
- Manual position logging for ground-truth data collection
- Physics engine modeling multipath, dielectric (capacitance-like) effects, and heterodyning

### Future Phases
- **Phase 1**: Direct XB7 admin UI scraping (10.0.0.1) — spectrum analyzer, per-device RSSI, channel stats
- **Phase 1.5**: 2D heatmaps from logged positions
- **Phase 2**: 3D RF tomography & AI reconstruction
- **Phase 3**: Passive motion detection & Doppler via heterodyning insights
- **Phase 4**: Open-source release + community sensing nodes

## 🛠️ Project Structure

```bash
IsoPhaseLab/
├── __init__.py
├── api.py                    # Main RadioVisionEngine facade
├── IsoPhaseLab_phase0.5.py   # Launcher script
├── core/
│   ├── __init__.py
│   ├── sensor.py             # WiFi signal acquisition (netsh + future XB7 scraper)
│   ├── physics.py            # Multipath, dielectric, heterodyning models
│   └── logger.py             # Data logging & CSV export
├── visualization/
│   └── dashboard.py          # Streamlit UI
├── README.md
└── requirements.txt
