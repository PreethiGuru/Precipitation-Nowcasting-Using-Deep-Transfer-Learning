**PRECIPITATION NOWCASTING USING DEEP TRANSFER LEARNING**

NEXRAD Level-II (Base) Data
Level-II (L2) data are grouped into three meteorological base quantities: reflectivity, mean radial velocity, and spectrum width. Additional categories include dual-polarization base data of differential reflectivity, correlation coefficient, and differential phase. Data is stored in files that typically contain four, five, six, or ten minutes of base data depending on the volume coverage pattern. A data file consists of a 24-byte volume scan header record followed by numerous 2,432-byte base data and message records.

Input location: Miami, Florida, USA
Output location: New Orleans, Louisiana, USA

Data source link: 
https://github.com/awslabs/open-data-docs/tree/main/docs/noaa/noaa-nexrad



----> A single file contains the following: (can be read using commands of PyArt --- pyart.io.read(filename).info())
altitude:
	data: <ndarray of type: float64 and shape: (1,)>
	long_name: Altitude
	standard_name: Altitude
	units: meters
	positive: up
altitude_agl: None
antenna_transition: None
azimuth:
	data: <ndarray of type: float64 and shape: (8280,)>
	units: degrees
	standard_name: beam_azimuth_angle
	long_name: azimuth_angle_from_true_north
	axis: radial_azimuth_coordinate
	comment: Azimuth of antenna relative to true north
elevation:
	data: <ndarray of type: float32 and shape: (8280,)>
	units: degrees
	standard_name: beam_elevation_angle
	long_name: elevation_angle_from_horizontal_plane
	axis: radial_elevation_coordinate
	comment: Elevation of antenna relative to the horizontal plane
fields:
	cross_correlation_ratio:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: ratio
		standard_name: cross_correlation_ratio_hv
		long_name: Cross correlation_ratio (RHOHV)
		valid_max: 1.0
		valid_min: 0.0
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	reflectivity:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: dBZ
		standard_name: equivalent_reflectivity_factor
		long_name: Reflectivity
		valid_max: 94.5
		valid_min: -32.0
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	differential_phase:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: degrees
		standard_name: differential_phase_hv
		long_name: differential_phase_hv
		valid_max: 360.0
		valid_min: 0.0
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	differential_reflectivity:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: dB
		standard_name: log_differential_reflectivity_hv
		long_name: log_differential_reflectivity_hv
		valid_max: 7.9375
		valid_min: -7.875
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	velocity:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: meters_per_second
		standard_name: radial_velocity_of_scatterers_away_from_instrument
		long_name: Mean doppler Velocity
		valid_max: 95.0
		valid_min: -95.0
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	spectrum_width:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: meters_per_second
		standard_name: doppler_spectrum_width
		long_name: Spectrum Width
		valid_max: 63.0
		valid_min: -63.5
		coordinates: elevation azimuth range
		_FillValue: -9999.0
	clutter_filter_power_removed:
		data: <ndarray of type: float32 and shape: (8280, 1832)>
		units: dB
		long_name: Clutter filter power removed
		standard_name: clutter_filter_power_removed
		valid_max: 73.0
		valid_min: 0.0
		coordinates: elevation azimuth range
		_FillValue: -9999.0
fixed_angle:
	data: <ndarray of type: float32 and shape: (15,)>
	long_name: Target angle for sweep
	units: degrees
	standard_name: target_fixed_angle
instrument_parameters:
	unambiguous_range:
		data: <ndarray of type: float32 and shape: (8280,)>
		units: meters
		comments: Unambiguous range
		meta_group: instrument_parameters
		long_name: Unambiguous range
	nyquist_velocity:
		data: <ndarray of type: float32 and shape: (8280,)>
		units: meters_per_second
		comments: Unambiguous velocity
		meta_group: instrument_parameters
		long_name: Nyquist velocity
latitude:
	data: <ndarray of type: float64 and shape: (1,)>
	long_name: Latitude
	standard_name: Latitude
	units: degrees_north
longitude:
	data: <ndarray of type: float64 and shape: (1,)>
	long_name: Longitude
	standard_name: Longitude
	units: degrees_east
nsweeps: 15
ngates: 1832
nrays: 8280
radar_calibration: None
range:
	data: <ndarray of type: float32 and shape: (1832,)>
	units: meters
	standard_name: projection_range_coordinate
	long_name: range_to_measurement_volume
	axis: radial_range_coordinate
	spacing_is_constant: true
	comment: Coordinate variable for range. Range to center of each bin.
	meters_to_center_of_first_gate: 2125.0
	meters_between_gates: 250.0
scan_rate: None
scan_type: ppi
sweep_end_ray_index:
	data: <ndarray of type: int32 and shape: (15,)>
	long_name: Index of last ray in sweep, 0-based
	units: count
sweep_mode:
	data: <ndarray of type: |S20 and shape: (15,)>
	units: unitless
	standard_name: sweep_mode
	long_name: Sweep mode
	comment: Options are: "sector", "coplane", "rhi", "vertical_pointing", "idle", "azimuth_surveillance", "elevation_surveillance", "sunscan", "pointing", "manual_ppi", "manual_rhi"
sweep_number:
	data: <ndarray of type: int32 and shape: (15,)>
	units: count
	standard_name: sweep_number
	long_name: Sweep number
sweep_start_ray_index:
	data: <ndarray of type: int32 and shape: (15,)>
	long_name: Index of first ray in sweep, 0-based
	units: count
target_scan_rate: None
time:
	data: <ndarray of type: float64 and shape: (8280,)>
	units: seconds since 2021-06-01T04:00:01Z
	standard_name: time
	long_name: time_in_seconds_since_volume_start
	calendar: gregorian
	comment: Coordinate variable for time. Time at the center of each ray, in fractional seconds since the global variable time_coverage_start
metadata:
	Conventions: CF/Radial instrument_parameters
	version: 1.3
	title: 
	institution: 
	references: 
	source: 
	history: 
	comment: 
	instrument_name: KAMX
	original_container: NEXRAD Level II
	vcp_pattern: 212

We only require fields -> reflectivity

Notebooks:
1) Reflectivity Numpy Array.ipynb
2) Data Visualization.ipynb
3) Models.ipynb -- contains Base CNN, CNN-FT and CNN-GRU
4) Contour Area (Supplementary)
5) Precipitation Classification (Supplementary)

The trained weights are not added to the zip file due to large file size (~750 MB)
Drive Link for CNN-GRU Trained weights: https://drive.google.com/drive/folders/1c7m6X8VnTsNBgXkZZwVnfgesdfvcoX2L?usp=sharing
