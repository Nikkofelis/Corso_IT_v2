# Location

- **Online**: utilise the NAS
- **Offline**
	- Air-Gapped-Device, physically separated device
	- S3 Cloud

# Type

- **Full**: Full copy of the data
- **Differential**: store just the modification on the main data
- **Incremental**: store just the modification on the previous version

# Retention

Multiple copy of data. Can be diversified by ==Version== or ==Time==.

## Method GFS

Grandfather-Father-Son

Keep a backup more and more frequently as the version is more recent.

## Disaster Recovery

Regularly backup data to different locations. The further the better.

## Business Continuity

Real time backup to different locations.