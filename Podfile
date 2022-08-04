install! 'cocoapods', :deterministic_uuids => false
platform :ios, '14.0'
use_frameworks!

target 'FSPlayer' do

pod 'ffmpeg-kit-ios-full', '~> 4.5.1'
pod 'SDL2', '~> 3.2.0'
pod 'MBProgressHUD'
pod 'Masonry'

end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['EXCLUDED_ARCHS[sdk=iphonesimulator*]'] = 'arm64'
        end
    end
end
