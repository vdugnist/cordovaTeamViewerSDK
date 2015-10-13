# cordovaTeamViewerSDK
A Cordova plugin that provides interface for native Android and iOS Team Viewer SDK.

## Installation

To install current plugin run a command from your cordova project folder:

    cordova plugin add https://github.com/vdugnist/cordovaTeamViewerSDK
  
## Usage
If you don't know how to get configurationId and token, refer to [before you start](https://integrate.teamviewer.com/en/develop/screen-sharing-sdk/android-tutorial/#H3_header_3) section in Team Viewer documentation.

### Open session with configuration id:

    var token = "your_token";
    var configurationId = "your_configuration_id";
    var name = "name_for_service_case";
    var description = "description_for_service_case"; // optional
    
    TeamViewerSDK.openSessionWithConfigurationId(token, configurationId, name, description,
      function(success) {
      // success block (optional)
    }, function(error) {
      // failure block (optional)
    });

### Open session with session code:

    var token = "your_token";
    var sessionCode = "session_code";

    TeamViewerSDK.openSessionWithSessionCode(token, sessionCode, function() {
      // success block (optional)
    }, function(error) {
      // failure block (optional)
    });
    
### Closing session

    TeamViewerSDK.closeCurrentSession();
    
    
## License

This plugin is released under MIT License. See LICENSE for details
