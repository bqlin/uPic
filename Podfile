source 'https://cdn.cocoapods.org/'
install! 'cocoapods', :generate_multiple_pod_projects => true
inhibit_all_warnings!
platform :osx, '10.12'


post_install do |installer|
  # Sign the Sparkle helper binaries to pass App Notarization.
  system("codesign --force -o runtime -s 'Developer ID Application' Pods/Sparkle/Sparkle.framework/Resources/Autoupdate.app/Contents/MacOS/Autoupdate")
  system("codesign --force -o runtime -s 'Developer ID Application' Pods/Sparkle/Sparkle.framework/Resources/Autoupdate.app/Contents/MacOS/fileop")
end

target 'uPic' do
# Comment the next line if you're not using Swift and don't want to use dynamic frameworks
use_frameworks!

    pod 'SwiftyJSON'
    pod 'Alamofire', '~> 5.0.2'
    pod 'MASShortcut'
    pod 'CryptoSwift', :git => "https://github.com/krzyzanowskim/CryptoSwift", :branch => "master"
    pod "SwiftyXMLParser", :git => 'https://github.com/yahoojapan/SwiftyXMLParser.git'
    pod 'Sparkle'
    pod 'Kingfisher'
    pod 'SnapKit', '~> 5.0.0'
    pod 'LoginServiceKit', :git => 'https://github.com/Clipy/LoginServiceKit.git'
    pod "libminipng"
    pod 'WCDB.swift'

end

