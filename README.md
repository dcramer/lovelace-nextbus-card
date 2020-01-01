# NextBus Card

A card which displays multiple public transit routes using the [NextBus sensors](https://www.home-assistant.io/integrations/nextbus/). This improves on a generic entity display making it appear more akin to a mobile phone widget, giving you more than just the next route's countdown.

![Screenshot](/screenshot.png?raw=true 'Example Card')

[![GitHub Release][releases-shield]][releases]
[![License][license-shield]](LICENSE.md)
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)

![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

## Options

| Name     | Type     | Requirement  | Description              | Default          |
| -------- | -------- | ------------ | ------------------------ | ---------------- |
| type     | string   | **Required** | `custom:nextbus-card`    |
| name     | string   | **Optional** | Card name                | `Public Transit` |
| entities | string[] | **Optional** | List of nextbus entities | `none`           |

## Developing with [devcontainer][devcontainer]

1. Fork and clone the repository.
2. Open the [devcontainer][devcontainer] and run `npm start` when it's ready.
3. The compiled `.js` file will be accessible on
   `http://127.0.0.1:5000/nextbus-card.js`.
4. On a running Home Assistant installation add this to your Lovelace
   `resources:`

```yaml
- url: 'http://127.0.0.1:5000/nextbus-card.js'
  type: module
```

_Change "127.0.0.1" to the IP of your development machine._

### Bonus

If you need a fresh test instance you can install a fresh Home Assistant instance inside the devcontainer as well.

1. Run the command `dc start`.
2. Home Assistant will install and will eventually be running on port `9123`
