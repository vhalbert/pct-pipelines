pipeline {
  agent {
    node {
      label 'maven'
    }
    
  }
  stages {
    stage('GC-1 License checks') {
      steps {
        git(url: 'http://git.app.eng.bos.redhat.com/git/jboss-prod-core/gates.git/', branch: 'master')
        load 'gates/licenses/RunGate.groovy'
      }
    }
    stage('GC-2 Crypto checks') {
      steps {
        load 'gates/crypto/RunGate.groovy'
      }
    }
    stage('GC-3 CVEs checks') {
      steps {
        load 'gates/cves/RunGate.groovy'
      }
    }
    stage('GC-4 Source code location checks') {
      steps {
        load 'gates/sourcecodelocation/RunGate.groovy'
      }
    }
    stage('GC-5 Dependencies checks') {
      steps {
        load 'gates/dependencies/RunGate.groovy'
      }
    }
    stage('GC-6 Unique version ID checks') {
      steps {
        load 'gates/uniqueversionsidentifiers/RunGate.groovy'
      }
    }
    stage('GC-7 Community artifact version checks ') {
      steps {
        load 'gates/communityartifactsversioning/RunGate.groovy'
      }
    }
    stage('GC-8 Version alignment checks') {
      steps {
        load 'gates/versionsalignmentanalysis/RunGate.groovy'
      }
    }
    stage('GC-9 Customer build-able source code checks ') {
      steps {
        load 'gates/buildablecustomersourcecode/RunGate.groovy'
      }
    }
    stage('GC-J1 JDK version checks') {
      steps {
        load 'gates/jdkversioning/RunGate.groovy'
      }
    }
    stage('GC-J2 Digital signature checks') {
      steps {
        load 'gates/jbosssignature/RunGate.groovy'
      }
    }
    stage('GC-J3 OpenJDK usage checks') {
      steps {
        load 'gates/openjdkusage/RunGate.groovy'
      }
    }
    stage('GC-M1 Maven version checks') {
      steps {
        load 'gates/mavenversioning/RunGate.groovy'
      }
    }
    stage('GC-M2 Maven repo validation checks') {
      steps {
        load 'gates/mavenrepovalidation/RunGate.groovy'
      }
    }
    stage('GC-A1 Build tool version checks') {
      steps {
        load 'gates/buildtoolversioning/RunGate.groovy'
      }
    }
    stage('GC-D1 Docker container workflow checks') {
      steps {
        load 'gates/dockercontainersworkflow/RunGate.groovy'
      }
    }
    stage('GC-D2 Dockerfile label checks') {
      steps {
        load 'gates/dockerfilelabeling/RunGate.groovy'
      }
    }
    stage('GC-D3 Dockerfile compliance checks') {
      steps {
        load 'gates/dockerfilecompliance/RunGate.groovy'
      }
    }
    stage('GC-D4 Docker image layering checks') {
      steps {
        load 'gates/dockercontainerlayering/RunGate.groovy'
      }
    }
    stage('GC-D5_6 Docker image freshness checks') {
      steps {
        load 'gates/dockercontainerhealthindex/RunGate.groovy'
      }
    }
    stage('GC-D7 Docker images allowed content checks') {
      steps {
        load 'gates/dockerimagesallowedcontent/RunGate.groovy'
      }
    }
    stage('GC-D8 Docker signed content checks') {
      steps {
        load 'gates/dockersignedcontent/RunGate.groovy'
      }
    }
    stage('GC-D9 Docker errata advisories checks') {
      steps {
        load 'gates/dockererrataadvisories/RunGate.groovy'
      }
    }
    stage('GC-D10 Docker image listed in PM sheet') {
      steps {
        load 'gates/dockerpmaskinputsheet/RunGate.groovy'
      }
    }
    stage('GC-D11 Openshift templates checks') {
      steps {
        load 'gates/dockeropenshifttemplates/RunGate.groovy'
      }
    }
    stage('GC-R1 RPM Errata advisories checks') {
      steps {
        load 'gates/rpmerrataadvisories/RunGate.groovy'
      }
    }
    stage('GC-R2 RPM Dependencies checks') {
      steps {
        load 'gates/rpmdependencies/RunGate.groovy'
      }
    }
    stage('GC-R3 RPM zip content checks') {
      steps {
        load 'gates/rpmandzipcontent/RunGate.groovy'
      }
    }
    stage('GC-R4 RPM Mead builds checks') {
      steps {
        load 'gates/rpmmeadbuilds/RunGate.groovy'
      }
    }
    stage('GI-1 Deliverables built on RH systems checks') {
      steps {
        load 'gates/deliverablesbuildsystem/RunGate.groovy'
      }
    }
    stage('GR-1 Deliverables included libraries checks') {
      steps {
        load 'gates/deliverablesincludedlibraries/RunGate.groovy'
      }
    }
    stage('GR-2 RH Product solutions checks') {
      steps {
        load 'gates/productsolutions/RunGate.groovy'
      }
    }
    stage('GR-3 Product support checks') {
      steps {
        load 'gates/productsupport/RunGate.groovy'
      }
    }
    stage('GR-4 Product documentation checks') {
      steps {
        load 'gates/productdocumentation/RunGate.groovy'
      }
    }
    stage('Store results') {
      steps {
        load 'gates/common/StorePipelineResults.groovy'
      }
    }
  }
}
